<link rel="stylesheet" href="style.css">
# BOHLALE RAMOLOTO 

<section>
<h2>MY NAME IS BOHLALE RAMOLOTO AND THIS IS MY PORTFOLIO</h2>
<h4> I am a passionate software engineer with multiple years of experience in the tech world.Starting from a small town,my curiosity for technology led to a degree in Computer Science and a career in innovative startups.I have developed everything from fintech applications to immersive gaming experiences. Committed to diversity in tech,I mentors young coders and organizes community hackathons. When not coding, you can find me exploring the outdoors or experimenting with IoT projects at home. With a blend of creativity and logic,I am dedicated to shaping the future of technology, one line of code at a time. </h4>
<section>
    
<section>
<h2>Personal Details</h2>
<h4>Name : Bohlale Christinah</h4>
<h4>Surname : Ramoloto</h4>
<h4>Age : 20 </h4>
<h4>Contact Details :  0720580982</h4>
<h4>E-mail : ramolotoc@gmail.com</h4>
<h4>Country : Republic Of South Africa</h4>
</section>

<section>
<h2>Education</h2>
<h3>UNIVERSITY OF LIMPOPO</h3>
<h4> BSC Mathematics And Computer Sciences </h4>
<h3>UNIVERSITY OF WITSWATERSRAND</h3>
<h4> HONORS DEGREE IN SOFTWARE DEVELOPMENT </h4>
</section>

<section>
<h2>Work Experience</h2>
<h4>software development </h4>
<h4>cybersecurity analyst</h4>
</section>

<section>
<h2>Projects</h2>
    
- GameQuest

- MindfulSpace
</section>

<section>
<h2>Contacts</h2>
<h4>phone number : 0720580982 </h4>
</section>


</head>
<body>

    <section>
        <h2>Contact Me</h2>
        <form action="send_email.php" method="POST">


            
            <section>
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>
            </section>


            <section>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            </section>


            <section>
            <label for="phone">Phone Number:</label>
            <input type="tel" id="phone" name="phone" required>
            </section>


            <section>
            <label for="comment">Comment:</label>
            <textarea id="comment" name="comment" required></textarea>
            </section>

            
            <button type="submit">Send</button>
        </form>
    </section>


    <section>
<a href="index.html">Home</a>
</section>


    
  <?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = htmlspecialchars($_POST['name']);
    $email = htmlspecialchars($_POST['email']);
    $phone = htmlspecialchars($_POST['phone']);
    $comment = htmlspecialchars($_POST['comment']);

    $to = "ramolotoc@gmail.com";
    $subject = "New Comment from $name";
    $message = "Name: $name\nEmail: $email\nPhone: $phone\nComment: $comment";
    $headers = "From: $email";

    if (mail($to, $subject, $message, $headers)) {
        echo "Message sent successfully!";
    } else {
        echo "Failed to send message.";
    }
} else {
    echo "Invalid request.";
}
?>
