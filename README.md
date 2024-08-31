<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Total Body Physio</title>
    <style>
        /* Add your CSS styles here */
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 1rem;
        }
        nav {
            background-color: #333;
            color: white;
            padding: 0.5rem;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin-right: 10px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
        }
        main {
            padding: 20px;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1rem;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Total Body Physio</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    <main>
        <h2>Welcome to Your Physiotherapy Clinic</h2>
        <p>We are dedicated to helping you achieve optimal physical health and well-being.</p>
        <!-- Add more content here -->
    </main>
    <footer>
        <p>&copy; 2024 Your Physiotherapy Clinic. All rights reserved.</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Total Body Physio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #35a79c;
            color: white;
            text-align: center;
            padding: 1rem;
        }
        nav {
            background-color: #2c3e50;
            color: white;
            padding: 0.5rem;
            text-align: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 0.5rem 1rem;
        }
        main {
            padding: 20px;
            max-width: 800px;
            margin: 0 auto;
            background-color: white;
        }
        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 1rem;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Total Body Physio</h1>
    </header>
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
    </nav>
    <main>
        <h2>Welcome to Total Body Physio</h2>
        <p>We are dedicated to helping you achieve optimal physical health and well-being through expert physiotherapy services.</p>
        <p>Our team of experienced physiotherapists is here to guide you on your journey to recovery and improved physical function.</p>
    </main>
    <footer>
        <p>&copy; 2024 Total Body Physio. All rights reserved.</p>
    </footer>
</body>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chatbot Flow Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        #chat {
            width: 400px;
            margin: 50px auto;
            border: 1px solid #ccc;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        #messages {
            height: 200px;
            overflow-y: scroll;
            border-bottom: 1px solid #ccc;
            margin-bottom: 20px;
            padding: 10px;
        }
        #user-input {
            width: calc(100% - 22px);
            padding: 10px;
        }
        .message {
            margin: 5px 0;
        }
        .message.user {
            text-align: right;
        }
        .message.bot {
            text-align: left;
        }
    </style>
</head>
<body>

<div id="chat">
    <div id="messages">
        <div class="message bot">Hi there! Welcome to Total Body Physio. How can I help you today?</div>
    </div>
    <input type="text" id="user-input" placeholder="Type your message here...">
</div>

<script>
    const messagesContainer = document.getElementById('messages');
    const userInput = document.getElementById('user-input');

    userInput.addEventListener('keypress', function(event) {
        if (event.key === 'Enter') {
            const message = userInput.value.trim();
            if (message) {
                displayMessage(message, 'user');
                processMessage(message);
                userInput.value = '';
            }
        }
    });

    function displayMessage(message, sender) {
        const messageElement = document.createElement('div');
        messageElement.classList.add('message', sender);
        messageElement.textContent = message;
        messagesContainer.appendChild(messageElement);
        messagesContainer.scrollTop = messagesContainer.scrollHeight;
    }

    function processMessage(message) {
        const lowerMessage = message.toLowerCase();
        let response = "I'm sorry, I didn't understand that. Can you please rephrase?";

        if (lowerMessage.includes('prices')) {
            response = `Our pricing is as follows:
            - ACC Consultation: $20 - $35
            - Private Consultation: $70 - $90
            - Telehealth Consultation: No charge with ACC.
            Would you like more details?`;
        } else if (lowerMessage.includes('where are you located')) {
            response = `We have several convenient locations:
            - Pakuranga: Lloyd Elsmore Leisure Centre
            - Flat Bush: 14 Fusion Road
            - Titirangi: Village Centre
            - Meadowlands: Cockle Bay Tennis Club.
            Would you like directions to any location?`;
        } else if (lowerMessage.includes('how do i cancel')) {
            response = "You can cancel your appointment by calling us, emailing us, or using the cancellation link provided in your confirmation email.";
        } else if (lowerMessage.includes('how do i book')) {
            response = `You can book an appointment by calling one of our clinics:
            - Pakuranga: 09 535 1932
            - Flat Bush: 09 265 2323
            - Titirangi: 09 817 7377
            - Meadowlands: 09 534 5990.
            Or book online here: [Book now](https://total-body-physio.au1.cliniko.com).`;
        }

        displayMessage(response, 'bot');
    }
</script>

</body>
</html>
