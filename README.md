# My-Project
HTML:
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="st1.css">
    <title>Campus Events Calendar</title>
</head>

<body>
    <header>
        <div class="container">
            <h1 id="heading">Campus Events Calendar</h1>
            <div class="topnav">
                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
                <div class="search-container">
                <input onkeyup="search_info()" type="text" id="searchbar" placeholder="Search...">
                <button id="searchButton" onclick="performSearch()" disabled hidden></button>
                </div>
            </div>
        </div>
    </header>

    <main class="container">
        <section id="welcome home" class="info">
            <h2>Welcome to Campus Events Calendar!</h2>
            <p>Discover and stay updated on all campus events and activities. Whether it's club meetings, sports games, workshops, or performances, we've got you covered.</p>
        </section>
        <h2 class="info">Upcoming Events: </h2>
        <section id="event-list" class="info">
        </section>
        

        <section class="info">
        <div id="event-list" class="info">
        </div>
        </section>
        <section>
        <h2>Add an Event: </h2>
        <div id="event-form">
        </div>
        </section>
        <section id="about" class="info">
            <h2>About Us</h2>
            <p>Welcome to Campus Events Calendar, your go-to platform for discovering and staying updated on all campus events and activities.</p>

            <p>Our mission is to provide a central hub where students, faculty, and staff can easily access information about upcoming events, workshops, performances, and more. Whether you're looking for a club meeting, a sports game, or a cultural event, we've got you covered.</p>

            <p>Feel free to explore our user-friendly calendar, submit your own events, and engage with the vibrant campus community.</p>

            <h3>Our Team</h3>
            <p>We are a passionate team dedicated to enhancing the campus experience through the power of events and community engagement. If you have any questions or suggestions, don't hesitate to reach out.</p>
            <h4>Our Members include:</h4>
            <p>
                <p class="member-name">1. Priyansh</p>
                <p class="member-position">Member</p>
                <p class="member-name">2. Arjun</p>
                <p class="member-position">Member</p>
                <p class="member-name">3. Harsha</p>
                <p class="member-position">Member</p>
            </p>
        </section>
        <section id="contact" class="info">
            <h2>Contact Us</h2>
            <p>Have a question, suggestion, or just want to get in touch? Fill out the form below, and we'll get back to you as soon as possible.</p>

            <form id="contact-form">
                <label for="name">Your Name:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Your Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Your Message:</label>
                <textarea id="message" name="message" rows="6" required></textarea>

                <button type="submit" reset>Submit</button>
            </form>
        </section>
        
    </main>
    <script src="sc.js"></script>
    <footer class="info">
        <p>&copy; Lovely Professional University</p>
    </footer>
</body>

</html>

CSS:
body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1rem 0;
}

main {
    margin-top: 20px;
}

#event-list {
    display: flex;
    flex-wrap: wrap;
}

.event-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 15px;
    margin: 10px;
    width: 300px;
    box-sizing: border-box;
}

#add-event {
    background-color: #333;
    color: #fff;
    padding: 10px;
    border: none;
    cursor: pointer;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1rem 0;
}
#about {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

    .topnav {
        overflow: hidden;
        background-color: #eae7dc;
      }
      
      .topnav a {
        float: left;
        display: block;
        color: #969595;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
      }
      
      .topnav a:hover {
        background-color: #ddd;
        color: black;
      }
      
      .topnav a.active {
        background-color: #2196F3;
        color: white;
      }
      
      .topnav input[type=text] {
        float: right;
        padding: 6px;
        border: none;
        margin-top: 8px;
        margin-right: 16px;
        font-size: 17px;
      }
      
      @media screen and (max-width: 600px) {
        .topnav a, .topnav input[type=text] {
          float: none;
          display: block;
          text-align: left;
          width: 100%;
          margin: 0;
          padding: 14px;
        }
        .topnav input[type=text] {
          border: 1px solid #ccc;
        }
      }

      .search-container{text-align:right;}
  
  #searchButton{text-align: right;
  padding-top: 10px;}

  #contact {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.member-position
{
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.member-name
{
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}

#welcome {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
.event-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 10px;
    margin-bottom: 10px;
}

#event-form {
    margin-top: 20px;
}

form {
    display: flex;
    flex-direction: column;
}

form input,
form textarea,
form button {
    margin-bottom: 10px;
    padding: 8px;
}

button {
    background-color: #333;
    color: #fff;
    cursor: pointer;
}
.search-container{text-align:right;}
  
  #searchButton{text-align: right;
  padding-top: 10px;}
  
  #heading
  {
    text-align: center;
  }

Javascript:
document.addEventListener('DOMContentLoaded', function () {
    const events = [
        { name: 'Community Clean-up Day', date: '2023-11-30', location: 'Auditorium', description: 'Volunteer your time to make a difference in the surrounding community' },
        { name: 'Concert on the Quad', date: '2023-12-05', location: 'Quad', description: 'Join us for a night of fun and live music on the campus quad' },
        { name: 'Champions Basketball Game', date: '2023-12-11', location: 'Basketball-Court', description: 'Cheer on your schools basketball team as they take on their biggest rivals!'}
    ];

    const eventListContainer = document.getElementById('event-list');
    const eventFormContainer = document.getElementById('event-form');

    function renderEvents() {
        eventListContainer.innerHTML = '';

        events.forEach(event => {
            const eventCard = document.createElement('div');
            eventCard.classList.add('event-card');
            eventCard.innerHTML = `
                <h2>${event.name}</h2>
                <p><strong>Date:</strong> ${event.date}</p>
                <p><strong>Location:</strong> ${event.location}</p>
                <p><strong>Description:</strong> ${event.description}</p>
            `;
            eventListContainer.appendChild(eventCard);
        });
    }

    function renderEventForm() {
        eventFormContainer.innerHTML = '';

        const eventForm = document.createElement('form');
        eventForm.innerHTML = `
            <label for="eventName" class="info">Event Name:</label>
            <input type="text" id="eventName" required>

            <label for="eventDate" class="info">Event Date:</label>
            <input type="date" id="eventDate" required>

            <label for="eventLocation" class="info">Event Location:</label>
            <input type="text" id="eventLocation" required>

            <label for="eventDescription" class="info">Event Description:</label>
            <textarea id="eventDescription" rows="4" required></textarea>

            <button type="button" onclick="addEvent()">Add Event</button>
        `;

        eventFormContainer.appendChild(eventForm);
    }

    window.addEvent = function () {
        const eventName = document.getElementById('eventName').value;
        const eventDate = document.getElementById('eventDate').value;
        const eventLocation = document.getElementById('eventLocation').value;
        const eventDescription = document.getElementById('eventDescription').value;

        if (!eventName || !eventDate || !eventLocation || !eventDescription) {
            alert('Please fill in all fields.');
            return;
        }

        events.push({ name: eventName, date: eventDate, location: eventLocation, description: eventDescription });

        renderEvents();

        document.getElementById('eventName').value = '';
        document.getElementById('eventDate').value = '';
        document.getElementById('eventLocation').value = '';
        document.getElementById('eventDescription').value = '';
    };

    renderEvents();
    renderEventForm();
});

function search_info() { 
    let input = document.getElementById('searchbar').value 
    input=input.toLowerCase(); 
    let x = document.getElementsByClassName('info'); 
      
    for (i = 0; i < x.length; i++) {  
        if (!x[i].innerHTML.toLowerCase().includes(input)) { 
            x[i].style.display="none"; 
        } 
        else { 
            x[i].style.display="list-item";                  
        } 
    } 
} 
