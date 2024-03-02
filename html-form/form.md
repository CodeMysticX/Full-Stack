# HTML Form with Congratulations Animation

This project showcases an HTML form with validation and a congratulations animation triggered upon successful form submission.

## Objective:

The objective of this project is to create an interactive HTML form with validation for various input fields, including name, age, gender selection, hobbies, and a brief introduction. Upon successful submission of the form, a colorful congratulations animation is displayed to provide visual feedback to the user.

## Features:

- **Form Validation:** Validation is implemented for all input fields to ensure that they are filled out correctly before submission.
- **Name Input:** The name input field allows for both first and last names, with validation to ensure at least one character is entered for each.
- **Age Input:** The age input field accepts numerical values only and is required.
- **Gender Selection:** Radio buttons for male and female gender selection, with validation to ensure one option is chosen.
- **Hobbies Selection:** Checkboxes for selecting multiple hobbies, including cricket, chess, volleyball, and football.
- **Brief Introduction:** A textarea for providing a brief introduction, which is required.
- **Congratulations Animation:** Upon successful submission of the form, a congratulations animation is displayed, featuring colorful paper cuts and ribbons falling from the top of the form.

## Usage:

1. **Filling out the Form:**
   - Fill out all required fields in the form, including name, age, gender, hobbies, and brief introduction.
   - Ensure that the name input accepts both first and last names separated by a space.
   - Select one gender option and choose one or more hobbies.
   - Provide a brief introduction in the textarea.

2. **Submitting the Form:**
   - Click the "Submit" button to submit the form.
   - If any required field is left empty or invalid data is entered, an alert will prompt the user to fill in all required fields.

3. **Congratulations Animation:**
   - Upon successful form submission, a congratulations animation will appear, adding a delightful visual feedback to signify successful completion of the form submission.

## CODE

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FORM</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "poppins", sans-serif;
        }
        :root {
            --primary-color: #c6c3c3;
            --second-color: #ffffff;
            --black-color: #000000;
            --text-color: #000000;
        }
        body {
            background-image: url("b3.jpg");
            background-repeat: no-repeat;
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        form {
            backdrop-filter: blur(25px);
            display: flex;
            flex-direction: column;
            width: 500px;
            height: 700px;
            margin-top: 7px;
            margin-bottom: 7px;
            border: 2px solid var(--primary-color);
            padding: 2em 2em 2em 2em;
            box-shadow: 0 0px 10px 2px rgba(0, 0, 0, 0.2);
        }
        .button {
            background-color: rgba(43, 43, 205, 0.991);
            color: aliceblue;
            align-self: center;
            width: 100%;
            height: 50px;
            background: #c6c3c3;
            font-size: 16px;
            font-weight: 500;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: 0.3s;
        }
        .button:hover {
            text-decoration: underline;
            background-color: blue;
            transition: 0.3s;
        }
        a {
            text-decoration: none;
            color: var(--second-color);
        }
        a:hover {
            text-decoration: underline;
        }
        .input-box {
            position: relative;
            display: flex;
            flex-direction: column;
            margin: 20px 0;
            box-shadow: #000000;
        }
        .input-field {
            width: 100%;
            height: 55px;
            font-size: 16px;
            background: transparent;
            color: var(--text-color);
            padding-inline: 20px 50px;
            border: 2px solid var(--primary-color);
            border-radius: 30px;
            outline: #000000;
        }
        #user {
            margin-bottom: 10px;
        }
        .label {
            position: absolute;
            top: -28px;
            left: 20px;
            transition: 0.2s;
            font-weight: bold;
        }
        p{
            font-weight: bold;
        }
        .input-field:focus~.label,
        .input-field:valid .label {
            position: absolute;
            top: -10px;
            left: 20px;
            font-size: 14px;
            background-color: var(--primary-color);
            border-radius: 30px;
            color: var(--black-color);
            padding: 0 10px;
        }
        .confetti-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 999;
        }
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #f00;
            border-radius: 50%;
            opacity: 0.8;
            animation: fall 3s linear infinite;
        }
        @keyframes fall {
            0% {
                transform: translateY(-100vh) rotateZ(0deg);
            }
            100% {
                transform: translateY(100vh) rotateZ(720deg);
            }
        }
    </style>
</head>
<body>
    <div class="forms">
        <form id="myForm">
            <div class="input-box">
                <input type="text" id="user" class="input-field" maxlength="20" minlength="2" pattern="^[A-Za-z]+[ ]?[A-Za-z]+$" required>
                <label for="name" class="label">Name</label>
                <i class="bx bx-user icon"></i>
            </div>
            <div class="input-box">
                <input type="number" id="age" class="input-field" maxlength="100" minlength="1" required>
                <label for="age" class="label">Age</label>
                <i class="bx bx-user icon"></i>
            </div>
            <div class="input-box">
                <p>Gender</p>
                <label for="Male">Male <input class="form-check-input" type="radio" id="Male" name="gender" required></label>
                <label for="Female">Female <input class="form-check-input" type="radio" id="Female" name="gender"></label>
            </div>
            <div class="input-box">
                <p>Hobbies</p>
                <label for="Cricket">Cricket <input class="form-check-input" type="checkbox" id="Cricket" name="hobbies"></label>
                <label for="Chess">Chess <input class="form-check-input" type="checkbox" id="Chess" name="hobbies"></label>
                <label for="Volleyball">Volleyball <input class="form-check-input" type="checkbox" id="Volleyball" name="hobbies"></label>
                <label for="Football">Football <input class="form-check-input" type="checkbox" id="Football" name="hobbies"></label><br>
            </div>
            <div class="input-box">
                <p>Brief Introduction</p>
                <textarea id="intro" cols="20" rows="5" required></textarea><br>
                <i class="bx bx-user icon"></i>
            </div>
            <div class="button">
                <button type="button" id="submitBtn" class="button">Submit</button>
            </div>
        </form>
    </div>
    <div class="confetti-container" id="confettiContainer"></div>

    <script>
        const form = document.getElementById('myForm');
        const submitBtn = document.getElementById('submitBtn');
        const confettiContainer = document.getElementById('confettiContainer');

        submitBtn.addEventListener('click', function() {
            if (form.checkValidity()) {
                alert('Form submitted successfully!');
                clearForm();
                showCongratulations();
            } else {
                alert('Please fill in all required fields.');
            }
        });

        function clearForm() {
            form.reset();
        }

        function showCongratulations() {
            const colors = ['#ff0000', '#00ff00', '#0000ff', '#ffff00', '#ff00ff', '#00ffff','#6420AA','#FF3EA5','#F5DD61','#9BCF53'];
            const numConfetti = 200;
            for (let i = 0; i < numConfetti; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.left = `${Math.random() * 100}%`;
                confetti.style.animationDuration = `${Math.random() * 3 + 1}s`;
                confettiContainer.appendChild(confetti);
            }
            setTimeout(() => {
                confettiContainer.innerHTML = '';
            }, 3000);
        }
    </script>
</body>
</html>
