
i. Student-developed procedure
```javascript
function formatBooks(books) {
    var output = "";
    for (var i = 0; i < books.length; i++) {
        output += books[i].Title + " by " + books[i].Author + " (" + books[i].Year + "), Genre: " + books[i].Genre + ", Dewey: " + books[i].Dewey + "\n";
    }
    return output;
}

```

ii. Procedure Call

```javascript
onEvent("submitSearchBtn", "click", function() {
    var searchTerm = getText("searchInput").trim().toLowerCase();
    
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

```

i. List

```javascript

var bookList = [];

onEvent("submitBookBtn", "click", function() {
    var title = getText("titleInput").trim();
    var author = getText("authorInput").trim();
    var genre = getText("genreInput").trim();
    var year = getText("yearInput").trim();
    
    if (!title || !author || !genre || !year) {
        setText("outputArea", "Error: All fields are required!");
        return;
    }

    if (isNaN(year)) {
        setText("outputArea", "Error: Year must be a number.");
        return;
    }
    
    var deweyCode = assignDewey(genre);
    var book = { Title: title, Author: author, Genre: genre, Year: parseInt(year), Dewey: deweyCode };
    bookList.push(book);

    setText("outputArea", "Book added successfully: " + title + " (Dewey: " + deweyCode + ")");
    clearTextFields();
});

```

ii. List being used

```javascript
onEvent("submitDisplayBtn", "click", function() {
    var genreFilter = getText("filterGenreInput").trim().toLowerCase();
    var yearFilter = getText("filterYearInput").trim();

    var results = bookList;
    
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

```

