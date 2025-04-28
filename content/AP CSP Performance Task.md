
```javascript

// Library collection (array of objects)
var bookList = [];

// Dewey Decimal Classification Mapping
var deweyDict = {
    "Computer Science": "000",
    "Philosophy": "100",
    "Religion": "200",
    "Social Sciences": "300",
    "Language": "400",
    "Science": "500",
    "Technology": "600",
    "Arts & Recreation": "700",
    "Literature": "800",
    "History & Geography": "900"
};

// Assigns a Dewey Decimal code based on genre
function assignDewey(genre) {
    if (deweyDict[genre]) {
        return deweyDict[genre];
    }
    return "Unknown"; // Default if genre is not found
}

// Switch screens function
function showScreen(screen) {
    setScreen(screen);
}


// Event listener for main menu buttons
onEvent("addBookBtn", "click", function() {
    showScreen("addBookScreen");
});

onEvent("SearchBtn", "click", function() {
    showScreen("searchScreen");
});

onEvent("displayBtn", "click", function() {
    showScreen("displayScreen");
});

// Back to home screen buttons
onEvent("backToHomeBtn1", "click", function() {
    showScreen("homeScreen");
});
onEvent("backToHomeBtn2", "click", function() {
    showScreen("homeScreen");
});
onEvent("backToHomeBtn3", "click", function() {
    showScreen("homeScreen");
});

// Add book functionality
onEvent("submitBookBtn", "click", function() {
    var title = getText("titleInput").trim();
    var author = getText("authorInput").trim();
    var genre = getText("genreInput").trim();
    var year = getText("yearInput").trim();
    //Check for all fields filled out
    if (!title || !author || !genre || !year) {
        setText("outputArea", "Error: All fields are required!");
        return;
    }

    if (isNaN(year)) {
        setText("outputArea", "Error: Year must be a number.");
        return;
    }
    var deweyCode = assignDewey(genre);
    //Assign and add book to book list with mapping
    var book = { Title: title, Author: author, Genre: genre, Year: parseInt(year), Dewey: deweyCode };
    bookList.push(book);

    setText("outputArea", "Book added successfully: " + title + " (Dewey: " + deweyCode + ")");
    clearTextFields();
});

// Clear input fields
function clearTextFields() {
    setText("titleInput", "");
    setText("authorInput", "");
    setText("genreInput", "");
    setText("yearInput", "");
}

// Search for books
onEvent("submitSearchBtn", "click", function() {
    var searchTerm = getText("searchInput").trim().toLowerCase();
    //Search algorithm
    var results = bookList.filter(function(book) {
        return book.Title.toLowerCase().includes(searchTerm) || 
               book.Author.toLowerCase().includes(searchTerm) || 
               book.Genre.toLowerCase().includes(searchTerm);
    });

    if (results.length > 0) {
        setText("searchResults", formatBooks(results));
    } else {
        setText("searchResults", "No books found.");
    }
});

// Display books (all or filtered)
onEvent("submitDisplayBtn", "click", function() {
    var genreFilter = getText("filterGenreInput").trim().toLowerCase();
    var yearFilter = getText("filterYearInput").trim();

    var results = bookList;
    //filter algorithm
    if (genreFilter) {
        results = results.filter(function(book) {
            return book.Genre.toLowerCase() === genreFilter;
        });
    }
    if (yearFilter && !isNaN(yearFilter)) {
        results = results.filter(function(book) {
            return book.Year === parseInt(yearFilter);
        });
    }

    if (results.length > 0) {
        setText("showBooks", formatBooks(results));
    } else {
        setText("showBooks", "No books found.");
    }
});

// Formats books into readable text that can be displayed
function formatBooks(books) {
    var output = "";
    //Clean up data
    for (var i = 0; i < books.length; i++) {
        output += books[i].Title + " by " + books[i].Author + " (" + books[i].Year + "), Genre: " + books[i].Genre + ", Dewey: " + books[i].Dewey + "\n";
    }
    return output;
}


```