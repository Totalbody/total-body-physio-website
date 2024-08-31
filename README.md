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
</html>
<div id="chatbot" style="position: fixed; bottom: 20px; right: 20px; width: 300px; border: 1px solid #ccc; border-radius: 5px; overflow: hidden;">
       <div id="chat-messages" style="height: 300px; overflow-y: auto; padding: 10px; background-color: #f9f9f9;"></div>
       <input type="text" id="user-input" placeholder="Type your message..." style="width: 100%; padding: 10px; border: none; border-top: 1px solid #ccc;">
   </div>

   <script>
   const chatMessages = document.getElementById('chat-messages');
   const userInput = document.getElementById('user-input');

   const botResponses = {
       "hello": "Hello! How can I help you today?",
       "services": "We offer a range of physiotherapy services including sports injury treatment, rehabilitation, and massage therapy.",
       "appointment": "To book an appointment, please call us at (123) 456-7890 or use our online booking system.",
       "location": "We are located at 123 Health Street, Wellness City. You can find directions on our Contact page.",
       "hours": "Our clinic is open Monday to Friday, 9am to 6pm, and Saturdays from 10am to 2pm."
   };

   function addMessage(message, isUser) {
       const messageElem = document.createElement('div');
       messageElem.textContent = message;
       messageElem.style.marginBottom = '10px';
       messageElem.style.padding = '5px';
       messageElem.style.borderRadius = '5px';
       messageElem.style.backgroundColor = isUser ? '#e6f2ff' : '#f0f0f0';
       chatMessages.appendChild(messageElem);
       chatMessages.scrollTop = chatMessages.scrollHeight;
   }

   userInput.addEventListener('keypress', function(e) {
       if (e.key === 'Enter') {
           const message = userInput.value.toLowerCase();
           addMessage(userInput.value, true);
           userInput.value = '';

           let botReply = "I'm sorry, I don't understand that question. Can you try asking about our services, appointments, location, or hours?";
           for (const [key, value] of Object.entries(botResponses)) {
               if (message.includes(key)) {
                   botReply = value;
                   break;
               }
           }

           setTimeout(() => addMessage(botReply, false), 500);
       }
   });
   </script>
<div id="chatbot" style="position: fixed; bottom: 20px; right: 20px; width: 300px; border: 1px solid #ccc; border-radius: 5px; overflow: hidden;">
       <div id="chat-messages" style="height: 300px; overflow-y: auto; padding: 10px; background-color: #f9f9f9;"></div>
       <input type="text" id="user-input" placeholder="Type your message..." style="width: 100%; padding: 10px; border: none; border-top: 1px solid #ccc;">
   </div>

   <script>
   const chatMessages = document.getElementById('chat-messages');
   const userInput = document.getElementById('user-input');

   const botResponses = {
       "hello": "Hello! How can I help you today?",
       "services": "We offer a range of physiotherapy services including sports injury treatment, rehabilitation, and massage therapy.",
       "appointment": "To book an appointment, please call us at (123) 456-7890 or use our online booking system.",
       "location": "We are located at 123 Health Street, Wellness City. You can find directions on our Contact page.",
       "hours": "Our clinic is open Monday to Friday, 9am to 6pm, and Saturdays from 10am to 2pm."
   };

   function addMessage(message, isUser) {
       const messageElem = document.createElement('div');
       messageElem.textContent = message;
       messageElem.style.marginBottom = '10px';
       messageElem.style.padding = '5px';
       messageElem.style.borderRadius = '5px';
       messageElem.style.backgroundColor = isUser ? '#e6f2ff' : '#f0f0f0';
       chatMessages.appendChild(messageElem);
       chatMessages.scrollTop = chatMessages.scrollHeight;
   }

   userInput.addEventListener('keypress', function(e) {
       if (e.key === 'Enter') {
           const message = userInput.value.toLowerCase();
           addMessage(userInput.value, true);
           userInput.value = '';

           let botReply = "I'm sorry, I don't understand that question. Can you try asking about our services, appointments, location, or hours?";
           for (const [key, value] of Object.entries(botResponses)) {
               if (message.includes(key)) {
                   botReply = value;
                   break;
               }
           }

           setTimeout(() => addMessage(botReply, false), 500);
       }
   });
   </script>
