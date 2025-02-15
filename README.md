<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1" />
  <title>Ujjwal Tyagi - Resume</title>
  <style>
    /* Import Google Fonts */
    @import url("https://fonts.googleapis.com/css?family=Varela+Round");
    @import url("https://fonts.googleapis.com/css?family=Open+Sans:400,300,600,700");

    *,
    *::before,
    *::after {
      box-sizing: border-box;
    }

    html,
    body {
      height: 100%;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Open Sans", sans-serif;
      font-size: 16px;
      line-height: 1.5em;
      background: #f4f4f4; /* Slight gray for outer background */
    }

    a {
      color: #66cc99;
      text-decoration: none;
    }

    .clearfix::before,
    .clearfix::after {
      content: "";
      display: table;
    }
    .clearfix::after {
      clear: both;
    }

    .bold {
      color: #4a4e51;
      font-weight: 400;
    }

    /* Resume Wrapper */
    .resume-wrapper {
      position: relative;
      text-align: center;
      min-height: 100vh; /* ensures it spans full height */
    }

    /* Container inside each section */
    .container {
      min-height: 600px;
    }

    /* Left Profile Section */
    .profile {
      background: #fff;       /* $profileBg */
      width: 40%;
      float: left;
      color: #9099a0;         /* $profileColor */
    }
    /* Responsive for smaller screens */
    @media (max-width: 850px) {
      .profile {
        width: 100%;
        float: none;
      }
    }

    /* Name area */
    .name-wrapper {
      float: left;
      width: 60%;
    }
    .name-wrapper h1 {
      font-size: 2.5em;
      text-align: left;
      font-family: "Varela Round", sans-serif;
      color: #4a4e51;         /* $boldColor */
      text-transform: uppercase;
      line-height: 1em;
      padding-top: 40px;
      margin: 0;
    }
    @media (max-width: 1200px) {
      .name-wrapper h1 {
        padding-top: 20px;
      }
    }
    @media (max-width: 450px) {
      .name-wrapper h1 {
        font-size: 1.8em;
        padding-top: 20px;
      }
    }

    /* Profile Picture Wrapper */
    .picture-resume-wrapper {
      width: 40%;
      float: left;
      display: block;
    }
    @media (max-width: 1200px) {
      .picture-resume-wrapper {
        width: 100%;
      }
    }
    .picture-resume {
      width: 220px;
      height: 220px;
      border-radius: 50%;
      display: table;
      position: relative;
      margin: 0 auto;
      vertical-align: middle;
    }
    @media (max-width: 1500px) {
      .picture-resume {
        width: 150px;
        height: 150px;
      }
    }
    @media (max-width: 1200px) {
      .picture-resume {
        width: 200px;
        height: 200px;
      }
    }
    @media (max-width: 450px) {
      .picture-resume {
        width: 180px;
        height: 180px;
      }
    }
    .picture-resume span {
      display: table-cell;
      vertical-align: middle;
      position: relative;
      z-index: 10;
      text-align: center;
    }
    .picture-resume img {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      object-fit: cover;
      display: block;
    }

    /* Contact Info */
    .contact-info {
      margin-top: 100px;
      font-weight: 300;
    }
    @media (max-width: 1200px) {
      .contact-info {
        margin-top: 70px;
      }
    }
    @media (max-width: 450px) {
      .contact-info {
        margin-top: 50px;
      }
    }
    .contact-info ul {
      list-style: none;
      margin: 0;
      padding: 0;
    }
    .list-titles {
      float: left;
      text-align: left;
      font-weight: 600;
      width: 40%;
      color: #4a4e51; /* $boldColor */
    }
    .list-content {
      float: left;
      width: 60%;
      text-align: left;
      font-weight: 300;
    }

    /* The SVG Bubbles */
    svg {
      width: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }
    .st0,
    .st1 {
      fill: #66cc99; /* $linkColor */
    }

    /* Right Experience Section */
    .experience {
      background: #3d3e42; /* $skillsBg */
      width: 60%;
      float: left;
      position: relative;
      color: #9099a0;     /* $skillsColor */
      font-weight: 300;
      min-height: 100vh; /* ensure it spans the height */
    }
    @media (max-width: 850px) {
      .experience {
        width: 100%;
        float: none;
      }
    }

    .experience-title {
      color: #66cc99; /* $linkColor */
      text-align: left;
      text-transform: uppercase;
      font-size: 1.2em;
      margin-bottom: 20px;
      font-weight: 400;
    }

    .company-wrapper {
      width: 30%;
      float: left;
      text-align: left;
      padding-right: 5%;
      margin-bottom: 60px;
    }
    @media (max-width: 450px) {
      .company-wrapper {
        width: 100%;
        margin-bottom: 20px;
      }
    }
    .job-wrapper {
      width: 70%;
      float: left;
      text-align: left;
      padding-right: 5%;
      margin-bottom: 60px;
    }
    @media (max-width: 450px) {
      .job-wrapper {
        width: 100%;
        margin-bottom: 40px;
      }
    }
    .job-wrapper .experience-title {
      color: white;
      margin-bottom: 15px;
    }

    /* Padding for each main section (profile/experience) */
    .section-padding {
      padding: 60px 60px 40px 40px;
    }
    @media (max-width: 850px) {
      .section-padding {
        padding: 80px 15% 40px 10%;
      }
    }
    @media (max-width: 450px) {
      .section-padding {
        padding: 40px 10% 20px 5%;
      }
    }

    /* Skills / Hobbies sections */
    .section-wrapper {
      width: 50%;
      float: left;
      text-align: left;
      color: #9099a0;
      font-weight: 300;
      margin-bottom: 20px;
    }
    @media (max-width: 450px) {
      .section-wrapper {
        width: 100%;
      }
    }
    .section-wrapper:nth-child(3) {
      padding-right: 8%;
    }
    .section-title {
      color: #66cc99;
      text-align: left;
      text-transform: uppercase;
      font-size: 1.2em;
      margin-bottom: 20px;
      font-weight: 400;
    }

    /* Skill Bars */
    .skill-percentage {
      margin-bottom: 10px;
      position: relative;
    }
    .skill-percentage::after {
      content: "";
      width: 100%;
      height: 6px;
      background: #4a4e51; /* $boldColor */
      display: block;
      margin-top: 3px;
    }
    .skill-percentage::before {
      content: "";
      height: 6px;
      background: #66cc99; /* $linkColor */
      position: absolute;
      margin-top: 3px;
      bottom: 0;
      width: 0; /* animated from 0 to target width */
    }

    /* Animations for skill bars */
    .skill-percentage:nth-child(1)::before {
      animation: skill_1 0.6s ease forwards;
    }
    .skill-percentage:nth-child(2)::before {
      animation: skill_2 0.6s ease forwards;
    }
    .skill-percentage:nth-child(3)::before {
      animation: skill_3 0.6s ease forwards;
    }
    .skill-percentage:nth-child(4)::before {
      animation: skill_4 0.6s ease forwards;
    }
    .skill-percentage:nth-child(5)::before {
      animation: skill_5 0.6s ease forwards;
    }
    .skill-percentage:nth-child(6)::before {
      animation: skill_6 0.6s ease forwards;
    }
    .skill-percentage:nth-child(7)::before {
      animation: skill_7 0.6s ease forwards;
    }

    @keyframes skill_1 {
      0% {
        width: 0;
      }
      100% {
        width: 80%;
      }
    }
    @keyframes skill_2 {
      0% {
        width: 0;
      }
      100% {
        width: 90%;
      }
    }
    @keyframes skill_3 {
      0% {
        width: 0;
      }
      100% {
        width: 50%;
      }
    }
    @keyframes skill_4 {
      0% {
        width: 0;
      }
      100% {
        width: 60%;
      }
    }
    @keyframes skill_5 {
      0% {
        width: 0;
      }
      100% {
        width: 70%;
      }
    }
    @keyframes skill_6 {
      0% {
        width: 0;
      }
      100% {
        width: 70%;
      }
    }
    @keyframes skill_7 {
      0% {
        width: 0;
      }
      100% {
        width: 70%;
      }
    }
  </style>
</head>
<body>
  <!-- WRAPPER -->
  <div class="resume-wrapper">
    <!-- LEFT PROFILE SECTION -->
    <section class="profile section-padding">
      <div class="container">
        <div class="picture-resume-wrapper">
          <div class="picture-resume">
            <!-- Profile Photo -->
            <span>
              <!-- Replace this with your own image path or URL -->
              <img src="WhatsApp Image 2025-02-15 at 18.02.08_cece6476.jpg" alt="Profile" />
            </span>
            <!-- SVG Bubbles -->
            <svg version="1.1" viewBox="0 0 350 350">
              <defs>
                <filter id="goo">
                  <feGaussianBlur in="SourceGraphic" stdDeviation="8" result="blur" />
                  <feColorMatrix
                    in="blur"
                    mode="matrix"
                    values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 21 -9"
                    result="cm"
                  />
                </filter>
              </defs>
              <g filter="url(#goo)">
                <circle id="main_circle" class="st0" cx="171.5" cy="175.6" r="130" />
                <circle id="circle" class="bubble0 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble1 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble2 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble3 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble4 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble5 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble6 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble7 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble8 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble9 st1" cx="171.5" cy="175.6" r="122.7" />
                <circle id="circle" class="bubble10 st1" cx="171.5" cy="175.6" r="122.7" />
              </g>
            </svg>
          </div>
          <div class="clearfix"></div>
        </div>
        <!-- NAME -->
        <div class="name-wrapper">
          <h1>Ujjwal <br />Tyagi</h1>
        </div>
        <div class="clearfix"></div>

        <!-- CONTACT INFO -->
        <div class="contact-info clearfix">
          <ul class="list-titles">
            <li>Call</li>
            <li>Mail</li>
          </ul>
          <ul class="list-content">
            <li>+91 9759659755</li>
            <li>davpshapur.ujjwaltyagi@gmail.com</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- RIGHT EXPERIENCE SECTION -->
    <section class="experience section-padding">
      <div class="container">
        <h3 class="experience-title">Experience</h3>

        <div class="experience-wrapper">
          <!-- 1st EXPERIENCE ONLY, NO DATES -->
          <div class="company-wrapper clearfix">
            <div class="experience-title">Company name</div>
          </div>
          <div class="job-wrapper clearfix">
            <div class="experience-title">Front End Developer</div>
            <div class="company-description">
              <!-- No text here -->
            </div>
          </div>
        </div>
        <!-- Skills & Hobbies -->
        <div class="section-wrapper clearfix">
          <h3 class="section-title">Skills</h3>
          <ul>
            <li class="skill-percentage">HTML / HTML5</li>
            <li class="skill-percentage">CSS / CSS3 / SASS / LESS</li>
            <li class="skill-percentage">Javascript</li>
            <li class="skill-percentage">Jquery</li>
            <li class="skill-percentage">Wordpress</li>
            <li class="skill-percentage">Photoshop</li>
            <li class="skill-percentage">Video Editing</li>
          </ul>
        </div>
        <div class="section-wrapper clearfix">
          <h3 class="section-title">Hobbies</h3>
          <p>Reading, Traveling, Music</p>
        </div>
      </div>
    </section>
    <div class="clearfix"></div>
  </div>

  <!-- BUBBLE ANIMATION JS -->
  <!-- Make sure TweenMax/GSAP is loaded BEFORE using it -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/1.20.4/TweenMax.min.js"></script>
  <script>
    // Some code thanks to @chrisgannon
    var select = function(s) {
      return document.querySelector(s);
    };

    function randomBetween(min, max) {
      var number = Math.floor(Math.random() * (max - min + 1) + min);
      return number !== 0 ? number : 0.5;
    }

    var tl = new TimelineMax();

    for (var i = 0; i < 20; i++) {
      var t = TweenMax.to(select('.bubble' + i), randomBetween(1, 1.5), {
        x: randomBetween(12, 15) * randomBetween(-1, 1),
        y: randomBetween(12, 15) * randomBetween(-1, 1),
        repeat: -1,
        repeatDelay: randomBetween(0.2, 0.5),
        yoyo: true,
        ease: Elastic.easeOut.config(1, 0.5)
      });
      tl.add(t, (i + 1) / 0.6);
    }

    // Start the timeline from a certain position if desired
    tl.seek(50);
  </script>
</body>
</html>
