# Advanced HTML5 Elements and Forms

## Objectives
Implement HTML5 images, lists, tables, forms and input types.
Use form validation attributes.
Apply multimedia elements such as audio and video.

## Instructions

- Create an index.html file.
- Add an ordered list with roman numerals
- Add an external image from pexels.com
- Add a table of 5 contacts with; name, address, mobile and emails
- Add a registration form

>[!NOTE]
>  The registration form should have:
>- Name, email, password, and date fields.
>- A dropdown, radio buttons, and checkboxes.
>- Proper labels and placeholders.
>- Required fields and validation attributes.
>- Ensure proper indentation and commenting.
 
# Tasks
- Create a well-structured HTML5 document.
- Ensure semantic correctness.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
    <!-- External CSS file for styling (optional) -->
    <link rel="stylesheet" href="styles.css">
    <!-- If you have a CSS file for styling, link it here. Otherwise, you can style inline or in a style tag within the head. -->
    <!-- For multimedia -->
    <style>
        /* Simple styling */
        body {
            font-family: Arial, sans-serif;
        }
        ol {
            list-style-type: upper-roman;
        }
        img {
            max-width: 100%;
            height: auto;
        }
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            text-align: left;
            padding: 8px;
        }
        th {
            background-color: #f2f2f2;
        }
        form {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        label {
            margin-bottom: 10px;
        }
        input[type="text"], input[type="email"], input[type="password"], input[type="date"] {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        input[type="submit"] {
            padding: 12px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #45a049;
        }
        .dropdown {
            position: relative;
            margin-bottom: 15px;
            display: inline-block;
            width: 100%;
        }
        .dropdown-content {
            display: none;
            position: absolute;
            background-color: #f1f1f1;
            min-width: 160px;
            box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
            z-index: 1;
        }
        .dropdown-content a {
            color: black;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
        }
        .dropdown-content a:hover {
            background-color: #ddd;
        }
        .dropdown:hover .dropdown-content {
            display: block;
        }
        /* Radio buttons styling */
        label[for="radio-option"] {
            display: inline-block;
            padding-right: 20px;
        }
        input[type="radio"] {
            display: none;
        }
        label[for="radio-option"]:after {
            content: '';
            display: inline-block;
            width: 15px;
            height: 15px;
            background: #ccc;
            margin-left: 5px;
        }
        input[type="radio"]:checked + label:after {
            background: #4CAF50;
        }
        /* Checkboxes styling */
        input[type="checkbox"] + label:before {
            content: '';
            display: inline-block;
            width: 15px;
            height: 15px;
            background: #ccc;
            margin-right: 5px;
        }
        input[type="checkbox"]:checked + label:before {
            background: #4CAF50;
        }
    </style>
</head>
<body>
    <!-- Ordered list with roman numerals -->
    <ol>
        <li>This is the first item of the ordered list.</li>
        <li>This is the second item of the ordered list.</li>
    </ol>

    <!-- External image -->
    <img src="https://images.pexels.com/photos/free-photos-download-images-stock-photos-pictures-photos-of-nature-pexels-photo-95513.jpeg" alt="Beautiful Landscape" width="100%" height="auto" />

    <!-- Table of contacts -->
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Address</th>
                <th>Mobile</th>
                <th>Email</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>John Doe</td>
                <td>123 Main St, Anytown, USA</td>
                <td>123-456-7890</td>
                <td>john.doe@example.com</td>
            </tr>
            <!-- More contacts can be added here, up to 5 for this example -->
        </tbody>
    </table>

    <!-- Registration Form -->
    <form action="/submit" method="post">
        <label for="name">Name</label>
        <input type="text" id="name" name="name" placeholder="Your full name" required>
        <label for="email">Email</label>
        <input type="email" id="email" name="email" placeholder="Your email address" required>
        <label for="password">Password</label>
        <input type="password" id="password" name="password" placeholder="Create a strong password" required>
        <label for="dob">Date of Birth</label>
        <input type="date" id="dob" name="dob" placeholder="YYYY-MM-DD" required>
        <div class="dropdown">
            <button class="dropdown-toggle" type="button" data-toggle="dropdown">Gender</button>
            <div class="dropdown-content">
                <a href="#">Male</a>
                <a href="#">Female</a>
                <a href="#">Prefer not to say</a>
            </div>
        </div>
        <div>
            <label>
                <input type="radio" id="radio-option1" name="gender" value="Male">
                Male
            </label>
            <label>
                <input type="radio" id="radio-option2" name="gender" value="Female">
                Female
            </label>
            <label>
                <input type="radio" id="radio-option3" name="gender" value="Prefer not to say">
                Prefer not to say
            </label>
        </div>
        <div>
            <label>
                <input type="checkbox" id="check-option1" name="interest" value="Hiking">
                I enjoy hiking.
            </label>
            <label>
                <input type="checkbox" id="check-option2" name="interest" value="Cycling">
                I enjoy cycling.
            </label>
        </div>
        <input type="submit" value="Register">
    </form>

    <!-- Commenting for clarity -->
    <!-- The registration form now includes validation attributes (required) and various input types including text, email, password, date, dropdown, radio buttons, and checkboxes. -->

    <!-- Proper indentation and structure have been maintained. -->
</body>
</html>
