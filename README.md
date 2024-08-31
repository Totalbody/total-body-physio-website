# Physiotherapy Website

This repository contains the code for my physiotherapy clinic website.

## Contents

- `index.html`: The main page of the website
- (List other files as you add them)

## How to Use

1. Clone this repository
2. Open `index.html` in a web browser to view the site locally
3. Edit the HTML and CSS to customize the site

## Deployment

This site is deployed using GitHub Pages. You can view it at [your-github-pages-url-here].

## Future Plans

- Add more pages (About, Services, Contact)
- Improve styling
- Add JavaScript for interactivity
- <!DOCTYPE html>
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
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Enhanced Chatbot Example</title>
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

        // Recognize keywords related to location and phone
        if (lowerMessage.includes('price') || lowerMessage.includes('cost')) {
            response = `Our pricing is as follows:
            - ACC Consultation: $20 - $35
            - Private Consultation: $70 - $90
            - Telehealth Consultation: No charge with ACC.
            Would you like more details?`;
        } else if (lowerMessage.includes('location') || lowerMessage.includes('where are you') || lowerMessage.includes('located')) {
            response = `We have several convenient locations:
            - **Pakuranga**: Lloyd Elsmore Leisure Centre
            - **Flat Bush**: 14 Fusion Road
            - **Titirangi**: Village Centre
            - **Meadowlands**: Cockle Bay Tennis Club

            Would you like directions to any location?`;
        } else if (lowerMessage.includes('phone') || lowerMessage.includes('contact number')) {
            response = `You can contact our clinics at the following numbers:
            - **Pakuranga**: 09 535 1932
            - **Flat Bush**: 09 265 2323
            - **Titirangi**: 09 817 7377
            - **Meadowlands**: 09 534 5990`;
        } else if (lowerMessage.includes('cancel') || lowerMessage.includes('reschedule')) {
            response = "You can cancel or reschedule your appointment by calling us, emailing us, or using the cancellation link provided in your confirmation email.";
        } else if (lowerMessage.includes('book') || lowerMessage.includes('appointment')) {
            response = `You can book an appointment by calling one of our clinics:
            - **Pakuranga**: 09 535 1932
            - **Flat Bush**: 09 265 2323
            - **Titirangi**: 09 817 7377
            - **Meadowlands**: 09 534 5990

            Or book online here: [Book now](https://total-body-physio.au1.cliniko.com).`;
        } else if (lowerMessage.includes('pakuranga')) {
            response = `**Pakuranga Clinic**:
            - Location: Lloyd Elsmore Leisure Centre
            - Hours: Mon-Thurs 7am - 6pm, Fri 7am - 3pm, Closed on weekends
            - Phone: 09 535 1932
            [View on Google Maps](https://goo.gl/maps/examplePakuranga)`;
        } else if (lowerMessage.includes('flat bush')) {
            response = `**Flat Bush Clinic**:
            - Location: 14 Fusion Road
            - Hours: Mon-Fri 7am - 6pm, Closed on weekends
            - Phone: 09 265 2323
            [View on Google Maps](https://goo.gl/maps/exampleFlatBush)`;
        } else if (lowerMessage.includes('titirangi')) {
            response = `**Titirangi Clinic**:
            - Location: Village Centre
            - Hours: Mon-Fri 7am - 6pm, Closed on weekends
            - Phone: 09 817 7377
            [View on Google Maps](https://goo.gl/maps/exampleTitirangi)`;
        } else if (lowerMessage.includes('meadowlands')) {
            response = `**Meadowlands Clinic**:
            - Location: Cockle Bay Tennis Club
            - Hours: Mon-Fri 7am - 6pm, Closed on weekends
            - Phone: 09 534 5990
            [View on Google Maps](https://goo.gl/maps/exampleMeadowlands)`;
        }

        displayMessage(response, 'bot');
    }
</script>

</body>
</html>
