<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>NYC Rideshare - Tri-Color Business Card</title>
<style>
    @page {
        size: Letter;
        margin: 0.5in;
    }
    body {
        font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
        background-color: #f4f5f7;
        color: #2b2d42;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    h2 {
        color: #555;
        margin-top: 40px;
    }
    /* Tri-Color All-Around Border & Card Setup */
    .card {
        width: 3.5in;
        height: 2in;
        background-color: #ffffff;
        /* Flashy all-around border */
        border: 4px solid #d90429; /* Crimson Red */
        outline: 3px solid #2b2d42; /* Charcoal Gray */
        outline-offset: -8px;
        position: relative;
        box-sizing: border-box;
        padding: 0.2in;
        margin-bottom: 20px;
        box-shadow: 0 10px 20px rgba(0,0,0,0.15);
        overflow: hidden;
    }
    
    /* Front of Card Layout */
    .front-header {
        text-align: center;
        border-bottom: 2px solid #2b2d42;
        padding-bottom: 5px;
        margin-bottom: 5px;
    }
    .front-header h1 {
        margin: 0;
        font-size: 13pt;
        color: #d90429;
        text-transform: uppercase;
        letter-spacing: 1px;
    }
    .front-header p {
        margin: 2px 0 0 0;
        font-size: 6.5pt;
        font-weight: bold;
        color: #2b2d42;
        letter-spacing: 1px;
    }
    
    .driver-section {
        display: flex;
        justify-content: space-between;
        margin-top: 8px;
    }
    .driver {
        width: 48%;
        text-align: center;
        background: rgba(244, 245, 247, 0.8);
        padding: 5px;
        border-radius: 4px;
    }
    .driver h3 {
        margin: 0;
        font-size: 9pt;
        color: #2b2d42;
    }
    .driver p {
        margin: 2px 0;
        font-size: 6.5pt;
        line-height: 1.2;
    }
    .driver .phone {
        color: #d90429;
        font-weight: bold;
        font-size: 7.5pt;
    }

    /* SVG Car Graphic Background Image */
    .car-watermark {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 150px;
        opacity: 0.05;
        z-index: 0;
    }

    /* Back of Card Layout */
    .back-content {
        text-align: center;
        position: relative;
        z-index: 2;
    }
    .back-content h3 {
        margin: 5px 0 10px 0;
        font-size: 11pt;
        color: #2b2d42;
    }
    .qr-container {
        display: inline-block;
        border: 2px solid #d90429;
        padding: 4px;
        background: #fff;
    }
    .back-content p {
        font-size: 7pt;
        font-weight: bold;
        color: #2b2d42;
        margin-top: 8px;
    }

</style>
</head>
<body>

    <h2>Front of Business Card</h2>
    <div class="card">
        <!-- Background Car Image -->
        <svg class="car-watermark" viewBox="0 0 100 50" xmlns="http://www.w3.org/2000/svg">
            <path d="M10,35 L15,20 L35,15 L70,15 L85,25 L90,35 Z" fill="none" stroke="#2b2d42" stroke-width="5"/>
            <circle cx="25" cy="35" r="7" fill="#d90429"/>
            <circle cx="75" cy="35" r="7" fill="#d90429"/>
        </svg>
        
        <div class="front-header" style="position:relative; z-index:2;">
            <h1>M&S Rideshare</h1>
            <p>PREMIUM NYC RIDE SERVICES | LUXURY</p>
        </div>
        <div class="driver-section" style="position:relative; z-index:2;">
            <div class="driver">
                <h3>Majharul Islam</h3>
                <p>Licensed NYC TLC Driver<br>7+ Years Experience</p>
                <p class="phone">+1 (939) 451-6893</p>
            </div>
            <div class="driver">
                <h3>Shipul Islam</h3>
                <p>Licensed NYC TLC Driver<br>7+ Years Experience</p>
                <p class="phone">+1 (347) 485-4904</p>
            </div>
        </div>
    </div>

    <h2>Back of Business Card</h2>
    <div class="card">
        <!-- Smaller Car Logo on Back -->
        <svg style="position:absolute; top: 15px; left: 15px; width:40px;" viewBox="0 0 100 50" xmlns="http://www.w3.org/2000/svg">
            <path d="M10,35 L15,20 L35,15 L70,15 L85,25 L90,35 Z" fill="none" stroke="#d90429" stroke-width="4"/>
            <circle cx="25" cy="35" r="6" fill="#2b2d42"/>
            <circle cx="75" cy="35" r="6" fill="#2b2d42"/>
        </svg>

        <div class="back-content">
            <h3>SCAN FOR SERVICES & BOOKING</h3>
            <div class="qr-container">
                <!-- QR Code linking to GitHub -->
                <img src="https://api.qrserver.com/v1/create-qr-code/?size=100x100&data=https://github.com/MajharulIslam/nyc-rideshare" alt="QR Code" width="80" height="80">
            </div>
            <p>Direct Link to Profiles & Amenities</p>
        </div>
    </div>

</body>
</html>
