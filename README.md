# smit.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smit Sadharakiya - Portfolio</title>
    <style>
        .active { display: block; }
        .hidden { display: none; }
        body { margin: 0; font-family: Arial, sans-serif; background-color: #f4f4f4; color: #2d3436; }
        .navbar { background-color: blue; overflow: hidden; display: flex; justify-content: center; padding: 10px 0; }
        .navbar a { color: white; text-decoration: none; padding: 14px 20px; font-size: 18px; }
        .navbar a:hover { background-color: #575757; border-radius: 5px; }
        .general { display: flex; align-items: center; justify-content: center; flex-wrap: wrap; padding: 40px; }
        .text { flex: 1; text-align: left; max-width: 500px; font-size: 24px; font-weight: bold; }
        .image { width: 300px; height: 300px; border-radius: 50%; object-fit: cover; margin-left: 20px; }
        .content { text-align: center; margin: 40px 20px; padding: 20px; background-color: lightblue; border-radius: 8px; box-shadow: 0px 4px 8px rgba(40, 108, 153, 0.47); max-width: 900px; margin-left: auto; margin-right: auto; }
        ul { text-align: left; max-width: 700px; margin: auto; list-style-type: "✅ "; }
        .contact-info { font-size: 18px; }
        .social-links a { text-decoration: none; color: #333; font-size: 20px; margin: 0 10px; display: inline-block; }
        .social-links a:hover { color: #0073e6; }
        .typewriter { font-size: 40px; border-right: 3px solid white; white-space: nowrap; overflow: hidden; display: inline-block; padding-right: 5px; }
        @media (max-width: 768px) { .general { flex-direction: column; text-align: center; } .text { text-align: center; margin-bottom: 20px; } .image { margin-left: 0; } }
    </style>
</head>
<body>
    <div class="navbar">
        <a onclick="showSection('about')" href="#about">About Me</a>
        <a onclick="showSection('achievements')" href="#achievements">My Achievements</a>
        <a onclick="showSection('projects')" href="#projects">My Projects</a>
        <a onclick="showSection('contact')" href="#contact">Contact Me</a>
    </div>

    <div class="general active" id="myself">
        <div class="text">
            <h1 class="typewriter">Hi, I am Smit Sadharakiya</h1>
        </div>
        

    <div class="content hidden" id="about">
        <h2>About Me</h2>
        <p>
            "Passionate IT Student | Full-Stack Developer | Problem Solver"<br>
            Hey, I'm Smit, an IT student with a drive to learn and build. I enjoy creating web applications and exploring new technologies.
            <br><br>
            Education:<br>
            🎓 Bachelor of Technology (B.Tech) in Information Technology<br>
            📍 [DDU Nadiad] (Year of Graduation: [2028])<br>
            <br>
            🏫 High School:<br>
            📍 [Knowledge High School] (Year of Completion: [2024])<br>
            <br>
            Key Skills:<br>
            ✅ Full-Stack Development: MERN Stack, Node.js, Express, SQL, Python>
            ✅ Problem Solving and Logical Thinking<br>
            ✅ Team Collaboration and Project Management<br>
            I believe in continuous learning, and I'm always looking for new challenges to tackle.
        </p>
    </div>

    <div class="content hidden" id="achievements">
        <h2>My Achievements</h2>
        <ul>
            <li>🥇 Completed NPTEL online course in C++</li>
            <li>📜 Completed Online Course of udemy in C</li>
            <li>🚀 Completed a 50 problems in Hackerrank</li>
            <li>💡 Created a Mobile App for School Event Management</li>
            
        </ul>
    </div>

    <div class="content hidden" id="projects">
        <h2>My Projects</h2>
        <ul>
            <li>
                <strong>IOT in Robotic Car
            
            </li>
            <li>
                <strong>IOT in Water Resource Management
                
            </li>
            <li>
                <strong>Dice Game</strong> - A fun dice-rolling game built with JavaScript.
               
            
                
  
        
    </div>

    <div class="content hidden" id="contact">
        <h2>Contact Me</h2>
        <p class="contact-info">
            📧 Email: <a href="mailto:smitsadharakiya@123.com">smitsadharakiya@example.com</a> <br>
            📞Mobile: +91 [9879796019] <br>
            📍 Location: [Nadiad], India
        </p>

        

    <script>
        function showSection(sectionId) {
            let sections = document.querySelectorAll('.content');
            sections.forEach(section => section.classList.remove('active'));
            sections.forEach(section => section.classList.add('hidden'));
            let activeSection = document.getElementById(sectionId);
            activeSection.classList.remove('hidden');
            activeSection.classList.add('active');
        }

        const text = "Hi, I am Smit Sadharakiya";
        let index = 0;
        let isDeleting = false;
        const typingSpeed = 150;
        const erasingSpeed = 100;
        const delayBetweenLoops = 1000;
        const typewriterElement = document.querySelector(".typewriter");

        function typeWriter() {
            if (!isDeleting) {
                typewriterElement.textContent = text.substring(0, index + 1);
                index++;
            } else {
                typewriterElement.textContent = text.substring(0, index - 1);
                index--;
            }

            if (!isDeleting && index === text.length) {
                setTimeout(() => isDeleting = true, delayBetweenLoops);
            } else if (isDeleting && index === 0) {
                isDeleting = false;
            }

            setTimeout(typeWriter, isDeleting ? erasingSpeed : typingSpeed);
        }

        document.addEventListener("DOMContentLoaded", typeWriter);
    </script>
</body>
</html>
