 Assignment 6.1 — Box Model Inspection
 1. Project structure
Create a folder named Assignment-6.1 with these files:


text
Assignment-6.1/
├── index.html
└── style.css
2. HTML code — index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.1 - Box Model Inspection</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>CSS Box Model Inspection</h1>
        <p>Explore content, padding, border, and margin.</p>
    </header>

    <main>
        <section class="cards">

            <div class="box box-one">
                <h2>Box 1: Content Box</h2>
                <p>
                    This box uses content-box. Padding and border
                    are added to the specified width.
                </p>
                <span>box-sizing: content-box;</span>
            </div>

            <div class="box box-two">
                <h2>Box 2: Border Box</h2>
                <p>
                    This box uses border-box. Padding and border
                    are included in the specified width.
                </p>
                <span>box-sizing: border-box;</span>
            </div>

            <div class="box box-three">
                <h2>Box 3: Custom Spacing</h2>
                <p>
                    This box has different padding, border, and
                    margin values to demonstrate spacing.
                </p>
                <span>box-sizing: border-box;</span>
            </div>

        </section>

        <section class="explanation">
            <h2>Understanding the Box Model</h2>
            <p><strong>Content:</strong> The text or other material inside an element.</p>
            <p><strong>Padding:</strong> Space between the content and the border.</p>
            <p><strong>Border:</strong> The outline surrounding the padding and content.</p>
            <p><strong>Margin:</strong> Space outside the border that separates elements.</p>
        </section>
    </main>

    <footer>
        <p>Assignment 6.1 | HTML and CSS</p>
    </footer>

</body>
</html>
3. CSS code — style.css

css

/* General styling */
* {
    font-family: Arial, sans-serif;
}

body {
    margin: 0;
    padding: 20px;
    background-color: #f1f5f9;
    color: #1e293b;
}

header {
    text-align: center;
    background-color: #1d4ed8;
    color: white;
    padding: 25px;
    margin-bottom: 30px;
    border-radius: 12px;
}

header h1 {
    margin-top: 0;
}

/* Arrange three boxes */
.cards {
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-wrap: wrap;
    gap: 25px;
}

/* Common box styling */
.box {
    width: 280px;
    background-color: white;
    border-radius: 10px;
}

.box h2 {
    margin-top: 0;
}

.box p {
    line-height: 1.6;
}

.box span {
    display: inline-block;
    background-color: #e2e8f0;
    padding: 8px;
    border-radius: 5px;
    font-size: 13px;
}

/* Box 1: content-box */
.box-one {
    box-sizing: content-box;
    padding: 15px;
    border: 4px solid #2563eb;
    margin: 10px;
    background-color: #eff6ff;
}

/* Box 2: border-box */
.box-two {
    box-sizing: border-box;
    padding: 25px;
    border: 6px solid #16a34a;
    margin: 20px;
    background-color: #f0fdf4;
}

/* Box 3: Different spacing */
.box-three {
    box-sizing: border-box;
    padding: 12px 30px;
    border: 8px dashed #ea580c;
    margin: 30px 10px;
    background-color: #fff7ed;
}

/* Explanation section */
.explanation {
    margin-top: 35px;
    padding: 25px;
    border: 2px solid #cbd5e1;
    background-color: white;
    border-radius: 10px;
}

.explanation h2 {
    color: #1d4ed8;
}

footer {
    text-align: center;
    margin-top: 25px;
    padding: 15px;
    color: #64748b;
}

/* Responsive layout */
@media (max-width: 600px) {
    body {
        padding: 12px;
    }

    .cards {
        flex-direction: column;
        align-items: center;
        gap: 15px;
    }

    .box {
        width: 100%;
        max-width: 340px;
    }
}
4. Expected output
The webpage will display a blue heading area, three colored cards with different borders and spacing, an explanation of the four box-model parts, and a footer.

CSS Box Model Inspection
Explore content, padding, border, and margin.

Box 1: Content Box
Padding and border are added to the specified width.

content-box

Box 2: Border Box
Padding and border are included in the width.

border-box

Box 3: Custom Spacing
A dashed border with different horizontal and vertical padding and margins.

border-box

Understanding the Box Model
Content: Text or other material inside an element.

Padding: Space inside the border.

Border: Outline around the content and padding.

Margin: Space outside the border.

Illustrative preview of the webpage design.

5. Box model diagram
The CSS box model has four layers. Use this diagram in your assignment explanation.

MARGIN
Outer space

BORDER
PADDING
CONTENT
Text, headings, images

Box model layers, from outside to inside: margin → border → padding → content.
6. Compare content-box and border-box
For a CSS width of 280px, with 20px padding on each side and a 5px border on each side:

Property

content-box

border-box

Declared width

280px

280px

Left + right padding

40px

40px

Left + right border

10px

10px

Actual outer width (excluding margin)

330px

280px

content-box: The declared width applies only to the content. Padding and borders increase the overall width.

border-box: The declared width includes the content, padding, and border.

Margin: Adds external spacing and is not included in either width calculation.

7. Inspect the box model in Chrome DevTools
Save index.html and style.css in the same folder.

Open index.html in Google Chrome.

Right-click the first card and select Inspect.

In DevTools, open the Computed tab and locate the Box Model diagram.

Click the second and third cards in the Elements panel to compare their padding, border, and margin.
Click a CSS value in the Styles panel and modify it to observe how the card changes.
8. Screenshot and submission
Take a screenshot of the complete webpage, then capture a second screenshot with Chrome DevTools open and the box model diagram visible. Label the four parts using an image editor, or add text annotations to the screenshot.

Your final submission should contain:

index.html

style.css

box-model-screenshot.png — webpage screenshot

box-model-annotated.png — screenshot with content, padding, border, and margin labeled

9. Conclusion for your assignment
The CSS box model describes how content, padding, border, and margin determine the size and spacing of HTML elements. The content-box property adds padding and border to the declared width, whereas border-box includes them within the declared width. Chrome DevTools helps inspect these values and understand how CSS changes affect the layout.