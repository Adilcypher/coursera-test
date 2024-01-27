<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Company Registration Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            width: 80%;
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
        }
        h2 {
            margin-top: 0;
        }
        input[type="text"], input[type="email"], select, textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }
        input[type="submit"] {
            background-color: #007BFF;
            color: #fff;
            border: none;
            padding: 10px 20px;
            border-radius: 3px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Company Registration Form</h2>
        <form id="registrationForm">
            <label for="companyName">Company Name</label>
            <input type="text" id="companyName" name="companyName" required>
            
            <label for="contactName">Contact Name</label>
            <input type="text" id="contactName" name="contactName" required>
            
            <label for="email">Email</label>
            <input type="email" id="email" name="email" required>
            
            <label for="industry">Industry</label>
            <select id="industry" name="industry">
                <option value="tech">Technology</option>
                <option value="finance">Finance</option>
                <option value="healthcare">Healthcare</option>
                <option value="other">Other</option>
            </select>
            
            <label for="comments">Comments</label>
            <textarea id="comments" name="comments" rows="4"></textarea>
            
            <input type="submit" value="Submit">
        </form>
    </div>

    <div id="confirmation" style="display: none;">
        <h2>Form Submitted Successfully</h2>
        <p>Thank you for registering your company with us!</p>
    </div>

    <script>
        const form = document.getElementById('registrationForm');
        const confirmation = document.getElementById('confirmation');

        form.addEventListener('submit', function (event) {
            event.preventDefault();
            form.style.display = 'none';
            confirmation.style.display = 'block';
        });
    </script>
</body>
</html>
