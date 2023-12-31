<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouTube </title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #e9e4e4; 
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px;
        }

        #youtube-logo {
            width: 100px;
            height: auto;
            cursor: pointer;
        }

        #search-bar {
            flex: 1;
            text-align: center;
        }

        #search-input {
            width: 80%;
            padding: 10px;
            border: none;
            border-radius: 5px;
        }

        #search-button {
            background-color: #FF0000;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        #search-button:hover {
            background-color: #FF3333;
        }

        #video-container {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        #video {
            width: 100%;
        }

        #channel-logo {
            display: block;
            max-width: 100px;
            max-height: 100px;
            border-radius: 50%;
            margin-top: 10px;
        }

        #channel-name {
            font-weight: bold;
            margin-top: 10px;
            margin-right: 10px; /* Add right margin for spacing */
        }

        #subscribe-button {
            background-color: #FF0000;
            color: #fff;
            padding: 10px 30px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin-top: 30px;
        }

        #subscribe-button:hover {
            background-color: #FF3333;
        }

        #channel-details {
            display: flex;
            align-items: center;
        }

        #additional-text {
            text-align: center;
            font-size: 18px;
            margin-top: 20px;
        }
        
        #channel-details p {
            margin-top: 10px; /* Add some space between Subscribe button and text */
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.4);
        }

        .modal-content {
            background-color: #fff;
            border-radius: 10px;
            width: 60%;
            max-width: 400px;
            margin: 0 auto;
            margin-top: 100px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body>
    <header>
        <a href="https://www.youtube.com" target="_blank">
            <img id="youtube-logo" src="images/download.png" alt="YouTube Logo">
        </a>
        <div id="search-bar">
            <input type="text" id="search-input" placeholder="Search on YouTube">
            <button id="search-button">Search</button>
        </div>
    </header>

    <div id="video-container">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/nFOjaKgVCl4?si=gRmm1JHBolMXw1XA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
       
        <div id="additional-text">
            <p>Railin Oligal | Blue Star | Ashok Selvan, Keerthi | Govind Vasantha | S.Jaya Kumar | Pa.Ranjith </p>
        </div>

        <div id="channel-details">
            <img id="channel-logo" src="images/download.png" alt="Channel Logo">
            <p id="channel-name">ABCD</p>
            <button id="subscribe-button" onclick="openRegistrationForm()">Subscribe</button>
            <br>
            
            <p>Presenting the Lyric Video of "Railin Oligal" from "Blue Star", Sung by Pradeep Kumar & Shakthisree Gopalan, Lyrics Written by Uma Devi, Music Composed by Govind Vasantha.</p>
        </div>

        <!-- Modal (Registration Form) -->
        <div id="registration-modal" class="modal">
            <div class="modal-content">
                <span id="close-modal" style="cursor: pointer;" onclick="closeRegistrationForm()">&times;</span>
                <h2>Registration Form</h2>
                <input type="text" placeholder="First Name"><br><br>
                <input type="text" placeholder="Last Name"><br><br>
                <input type="text" placeholder="Phone Number"><br><br>
                <input type="email" placeholder="Email"><br><br>
                <label for="gender">Gender:</label><br>
                <input type="radio" name="gender" value="male"> Male
                <input type="radio" name="gender" value="female"> Female
                <input type="radio" name="gender" value="other"> Other<br><br>
                <label for="interests">Interests:</label><br>
                <input type="checkbox" name="interest" value="music"> Music
                <input type="checkbox" name="interest" value="sports"> Sports
                <input type="checkbox" name="interest" value="movies"> Movies<br><br>
                <button id="submit-button">Submit</button>
            </div>
        </div>
    </div>

    <script>
        function openRegistrationForm() {
            document.getElementById("registration-modal").style.display = "block";
        }

        function closeRegistrationForm() {
            document.getElementById("registration-modal").style.display = "none";
        }
    </script>
</body>
</html>
