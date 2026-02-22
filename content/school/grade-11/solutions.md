# Math Problem Solutions

---

## Problem 35 — Photography (Hawk Distance)

**Setup:** Jeff is taking pictures of a hawk that is 150 ft above him. The hawk will fly directly over Jeff. Let *d* be the distance from Jeff to the hawk, and *θ* be the angle of elevation from Jeff's camera to the hawk.

From the diagram, the hawk is at a height of 150 ft. The relationship between *d*, *θ*, and the height forms a right triangle where the opposite side (height) is 150 ft and the hypotenuse is *d*.

### Part (a): Write *d* as a function of *θ*

Using the sine ratio:

$$\sin(\theta) = \frac{\text{opposite}}{\text{hypotenuse}} = \frac{150}{d}$$

Solving for *d*:

$$d = \frac{150}{\sin(\theta)}$$

$$\boxed{d(\theta) = 150\csc(\theta)}$$

### Part (b): Graph the function on the interval 0 < θ < π

Key features of d(θ) = 150 csc(θ) on (0, π):
- Vertical asymptotes at θ = 0 and θ = π
- Minimum value at θ = π/2, where d = 150 csc(π/2) = 150(1) = 150
- The graph is a U-shaped curve opening upward with minimum at (π/2, 150)
- As θ → 0⁺ or θ → π⁻, d → ∞

| θ      | d = 150 csc(θ) |
|--------|-----------------|
| π/6    | 150 csc(π/6) = 150(2) = 300 |
| π/4    | 150 csc(π/4) = 150(√2) ≈ 212.1 |
| π/3    | 150 csc(π/3) = 150(2√3/3) ≈ 173.2 |
| π/2    | 150 csc(π/2) = 150(1) = 150 |
| 2π/3   | 150 csc(2π/3) ≈ 173.2 |
| 3π/4   | 150 csc(3π/4) ≈ 212.1 |
| 5π/6   | 150 csc(5π/6) = 300 |

*(The graph is a csc curve with minimum at 150, symmetric about θ = π/2.)*

### Part (c): How far away is the hawk when θ = 45°?

$$d = 150\csc(45°) = \frac{150}{\sin(45°)} = \frac{150}{\frac{\sqrt{2}}{2}} = \frac{150 \cdot 2}{\sqrt{2}} = \frac{300}{\sqrt{2}} = \frac{300\sqrt{2}}{2} = 150\sqrt{2}$$

$$\boxed{d \approx 212.1 \text{ ft}}$$

---

## Problems 44–47 — Match Each Function With Its Graph

The four graphs (a, b, c, d) need to be matched with these functions:

- **44.** y = csc(x/3 + π/4) − 2
- **45.** y = sec(x/3 + π/4) − 2
- **46.** y = cot(2x − π/4) − 2
- **47.** y = tan(2x − π/4) − 2

**Analysis of each function:**

### Problem 44: y = csc(x/3 + π/4) − 2

- This is a **cosecant** function.
- B = 1/3, so the period = 2π / (1/3) = **6π**
- Phase shift = −π/4 ÷ (1/3) = −3π/4 (shift left 3π/4)
- Vertical shift: down 2
- The x-axis scale on graphs (a) and (c) extends to ±4π, which accommodates period 6π.
- Cosecant has U-shaped curves opening up and down.
- Graph **(a)** shows a csc-type curve with long period and vertical shift down 2.

$$\boxed{44 \to \text{Graph (a)}}$$

### Problem 45: y = sec(x/3 + π/4) − 2

- This is a **secant** function.
- B = 1/3, so the period = 2π / (1/3) = **6π**
- Phase shift = −3π/4 (shift left 3π/4)
- Vertical shift: down 2
- Secant has U-shaped curves similar to csc but shifted by half a period relative to csc.
- Graph **(c)** shows a sec-type curve with long period and vertical shift down 2.

$$\boxed{45 \to \text{Graph (c)}}$$

### Problem 46: y = cot(2x − π/4) − 2

- This is a **cotangent** function.
- B = 2, so the period = π/2
- Phase shift = (π/4)/2 = π/8 (shift right π/8)
- Vertical shift: down 2
- Cotangent is decreasing between consecutive vertical asymptotes.
- Graph **(b)** shows a cot-type curve (decreasing branches) with short period and vertical shift down 2.

$$\boxed{46 \to \text{Graph (b)}}$$

### Problem 47: y = tan(2x − π/4) − 2

- This is a **tangent** function.
- B = 2, so the period = π/2
- Phase shift = (π/4)/2 = π/8 (shift right π/8)
- Vertical shift: down 2
- Tangent is increasing between consecutive vertical asymptotes.
- Graph **(d)** shows a tan-type curve (increasing branches) with short period and vertical shift down 2.

$$\boxed{47 \to \text{Graph (d)}}$$

---

## Problems 52–55 — Write an Equation Given Period, Phase Shift, and Vertical Shift

### Problem 52: function: sec; period: 3π; ps: 0; vs: 2

The general form of secant is: y = sec(Bx − C) + D

- **Period** = 2π/B = 3π → B = 2π/(3π) = **2/3**
- **Phase shift** = C/B = 0 → C = 0
- **Vertical shift** D = 2

$$\boxed{y = \sec\!\left(\frac{2}{3}x\right) + 2}$$

### Problem 53: function: tan; period: π/2; ps: π/4; vs: −1

The general form of tangent is: y = tan(Bx − C) + D

- **Period** = π/B = π/2 → B = π/(π/2) = **2**
- **Phase shift** = C/B = π/4 → C = B · (π/4) = 2 · (π/4) = **π/2**
- **Vertical shift** D = −1

$$\boxed{y = \tan\!\left(2x - \frac{\pi}{2}\right) - 1}$$

### Problem 54: function: csc; period: π/4; ps: −π; vs: 0

The general form of cosecant is: y = csc(Bx − C) + D

- **Period** = 2π/B = π/4 → B = 2π/(π/4) = **8**
- **Phase shift** = C/B = −π → C = B · (−π) = 8 · (−π) = **−8π**
- **Vertical shift** D = 0

$$\boxed{y = \csc(8x + 8\pi)}$$

*Note: Since csc has period 2π in its argument, and 8·(−π) shifts by a full multiple of the internal period, this simplifies to y = csc(8x). However, the non-simplified form showing the phase shift is:*

$$y = \csc\!\left(8x + 8\pi\right) = \csc(8x)$$

$$\boxed{y = \csc(8x + 8\pi) \text{ or equivalently } y = \csc(8x)}$$

### Problem 55: function: cot; period: 3π; ps: π/2; vs: 4

The general form of cotangent is: y = cot(Bx − C) + D

- **Period** = π/B = 3π → B = π/(3π) = **1/3**
- **Phase shift** = C/B = π/2 → C = B · (π/2) = (1/3)(π/2) = **π/6**
- **Vertical shift** D = 4

$$\boxed{y = \cot\!\left(\frac{1}{3}x - \frac{\pi}{6}\right) + 4}$$

---

## Problem 76 — Right Triangle: Find *b* given c = 14 and a 30° angle

From the figure, we have a right triangle with:
- Hypotenuse c = 14
- Angle = 30°
- Side *b* is adjacent to the 30° angle (the base)

Using cosine:

$$\cos(30°) = \frac{\text{adjacent}}{\text{hypotenuse}} = \frac{b}{c} = \frac{b}{14}$$

$$b = 14\cos(30°) = 14 \cdot \frac{\sqrt{3}}{2} = 7\sqrt{3}$$

$$\boxed{b = 7\sqrt{3} \quad \textbf{(Answer: J)}}$$

---

## Problem 77 — Identify the Equation from the Graph

From the graph:
- The curve has vertical asymptotes at θ = 0 and θ = π/2 (and repeats with period π)
- The curve is **decreasing** between asymptotes — this identifies it as a **cotangent** function
- The graph appears to pass through (π/4, 0), meaning the curve is shifted
- Standard cot(θ) has a zero at π/2, but this graph's zero is at π/4

Checking the options:

- **A.** y = cot(θ + π/4): Zero when θ + π/4 = π/2 → θ = π/4. Asymptote when θ + π/4 = 0 → θ = −π/4. ✗ (asymptote location doesn't match)
- **B.** y = cot(θ − π/4): Zero when θ − π/4 = π/2 → θ = 3π/4. ✗
- **C.** y = tan(θ + π/4): Tangent is increasing. ✗
- **D.** y = tan(θ − π/4): Zero when θ − π/4 = 0 → θ = π/4. ✓ Asymptote when θ − π/4 = −π/2 → θ = −π/4 and when θ − π/4 = π/2 → θ = 3π/4.

Wait — re-examining the graph more carefully: the curve passes through approximately (π/4, 0) and appears to be **increasing** through that zero (going from bottom-left to top-right between asymptotes). That is characteristic of **tangent**, not cotangent.

The asymptotes appear to be near θ = −π/4 and θ = 3π/4, and the function increases between them, passing through zero at θ = π/4.

For y = tan(θ − π/4):
- Zero at θ = π/4 ✓
- Asymptotes at θ − π/4 = ±π/2 → θ = −π/4 and θ = 3π/4 ✓
- Increasing between asymptotes ✓

$$\boxed{\textbf{D. } y = \tan\!\left(\theta - \frac{\pi}{4}\right)}$$

---

## Problem 78 — Find θ given sin θ = −1/2 and π < θ < 3π/2

We need to find θ such that:
- sin θ = −1/2
- π < θ < 3π/2 (third quadrant)

The reference angle for sin θ = 1/2 is π/6 (since sin(π/6) = 1/2).

In the **third quadrant** (π < θ < 3π/2), sine is negative, and:

$$\theta = \pi + \frac{\pi}{6} = \frac{6\pi}{6} + \frac{\pi}{6} = \frac{7\pi}{6}$$

**Verification:** sin(7π/6) = sin(π + π/6) = −sin(π/6) = −1/2 ✓

$$\boxed{\theta = \frac{7\pi}{6} \quad \textbf{(Answer: G)}}$$

---
