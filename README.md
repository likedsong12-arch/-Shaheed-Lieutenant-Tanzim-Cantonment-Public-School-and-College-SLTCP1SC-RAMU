<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SLTCPSC RAMU - Student Registration</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #db4b4b 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .form-container {
            background: white;
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            padding: 40px;
            width: 100%;
            max-width: 500px;
            position: relative;
            overflow: hidden;
        }
        
        .form-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4, #45b7d1);
        }
        
        .school-header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .school-logo {
            width: 100px;
            height: 100px;
            margin: 0 auto 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }
        
        .school-logo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
        }
        
        h1 {
            color: #333;
            font-size: 24px;
            margin-bottom: 10px;
            line-height: 1.2;
        }
        
        .subtitle {
            color: #666;
            font-size: 16px;
            margin-bottom: 20px;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            color: #333;
            font-weight: 600;
            font-size: 14px;
        }
        
        input[type="number"] {
            width: 100%;
            padding: 15px;
            border: 2px solid #e1e5e9;
            border-radius: 10px;
            font-size: 16px;
            transition: all 0.3s ease;
            background: #f8f9fa;
        }
        
        input[type="number"]:focus {
            outline: none;
            border-color: #667eea;
            background: white;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }
        
        .submit-btn {
            width: 100%;
            padding: 15px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
        }
        
        .submit-btn:active {
            transform: translateY(0);
        }
        
        .prank-banner {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #ff6b6b, #ee5a24);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            animation: slideDown 0.5s ease-out;
        }
        
        .prank-content {
            text-align: center;
            color: white;
            padding: 40px;
            background: rgba(0,0,0,0.2);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            animation: bounce 0.6s ease-out;
        }
        
        .prank-title {
            font-size: 4em;
            font-weight: bold;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .prank-message {
            font-size: 1.5em;
            margin-bottom: 30px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
        }
        
        .close-btn {
            padding: 15px 30px;
            background: white;
            color: #ff6b6b;
            border: none;
            border-radius: 25px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .close-btn:hover {
            background: #f1f1f1;
            transform: scale(1.05);
        }
        
        @keyframes slideDown {
            from {
                transform: translateY(-100%);
            }
            to {
                transform: translateY(0);
            }
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-20px);
            }
            60% {
                transform: translateY(-10px);
            }
        }
        
        .required {
            color: #ff6b6b;
        }
        
        .info-text {
            font-size: 14px;
            color: #666;
            margin-top: 20px;
            text-align: center;
            line-height: 1.5;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <div class="school-header">
            <div class="school-logo">
                <img id="schoolLogo" src="" alt="School Logo">
            </div>
            <h1>Shaheed Lieutenant Tanzim Cantonment Public School and College</h1>
            <p class="subtitle">SLTCPSC RAMU - Student Registration Portal</p>
        </div>
        
        <form id="registrationForm">
            <div class="form-group">
                <label for="schoolId">Student School ID <span class="required">*</span></label>
                <input type="number" id="schoolId" name="schoolId" required placeholder="Enter your school ID (numbers only)" min="1">
            </div>
            
            <button type="submit" class="submit-btn">Complete Registration</button>
        </form>
        
        <p class="info-text">
            Please use your official school ID for registration. 
            You will receive confirmation and further instructions via your registered contact.
        </p>
    </div>

    <div class="prank-banner" id="prankBanner">
        <div class="prank-content">
            <div class="prank-title">🎉 PRANKED! 🎉</div>
            <div class="prank-message">
                TOR NANANI TOI EKTA GATA . NADIA TOI ATO GADA 
                KIBABH ? 
            </div>
            <button class="close-btn" onclick="closePrank()">Got me good! 😂</button>
        </div>
    </div>

    <script>
        // Load the school logo from URL
        function loadSchoolLogo() {
            const logoImg = document.getElementById('schoolLogo');
            const logoUrl = 'https://scontent.fcgp7-1.fna.fbcdn.net/v/t39.30808-1/465609910_1039113178234400_6574594893766783494_n.jpg?stp=dst-jpg_s200x200_tt6&_nc_cat=107&ccb=1-7&_nc_sid=2d3e12&_nc_ohc=9ENLSNfi9K8Q7kNvwGj5oOY&_nc_oc=Adn3YkMbagHeiENywXQHmtQ3lgOrddRBdrz07s4XlXhiWF1K8m796ppIyrAs7tbept4&_nc_zt=24&_nc_ht=scontent.fcgp7-1.fna&_nc_gid=m6jlUGmvrsPBS7IS9LMT8A&oh=00_AfU5lAFHujQ-hRLpUwTBiSE2hYtJgZ7VkTvQF7bmdN5pQQ&oe=68BCAA48';
            
            logoImg.src = logoUrl;
            logoImg.style.display = 'block';
            
            // Handle error if image fails to load
            logoImg.onerror = function() {
                console.log('Could not load logo from URL, using fallback');
                const logoContainer = document.querySelector('.school-logo');
                logoContainer.innerHTML = 'SLTCPSC';
                logoContainer.style.background = 'linear-gradient(135deg, #2c5530, #4a7c59)';
                logoContainer.style.color = 'white';
                logoContainer.style.fontSize = '18px';
                logoContainer.style.fontWeight = 'bold';
                logoContainer.style.textAlign = 'center';
                logoContainer.style.lineHeight = '1.1';
                logoContainer.style.display = 'flex';
                logoContainer.style.alignItems = 'center';
                logoContainer.style.justifyContent = 'center';
            };
            
            logoImg.onload = function() {
                console.log('School logo loaded successfully!');
            };
        }
        
        // Initialize logo when page loads
        window.addEventListener('load', loadSchoolLogo);
        
        let userSchoolId = '';
        
        document.getElementById('registrationForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            userSchoolId = document.getElementById('schoolId').value;
            console.log('School ID entered:', userSchoolId); // Debug log
            
            // Check if it's a valid integer
            if (userSchoolId && userSchoolId.trim() !== '' && Number.isInteger(Number(userSchoolId)) && Number(userSchoolId) > 0) {
                showPrank();
            } else {
                alert('Please try again! Enter a valid school ID (numbers only)');
                document.getElementById('schoolId').focus();
            }
        });
        
        // Alternative trigger - also listen for button click
        document.querySelector('.submit-btn').addEventListener('click', function(e) {
            e.preventDefault();
            
            userSchoolId = document.getElementById('schoolId').value;
            
            // Check if it's a valid integer
            if (userSchoolId && userSchoolId.trim() !== '' && Number.isInteger(Number(userSchoolId)) && Number(userSchoolId) > 0) {
                showPrank();
            } else {
                alert('Please try again! Enter a valid school ID (numbers only)');
                document.getElementById('schoolId').focus();
            }
        });
        
        function showPrank() {
            const prankBanner = document.getElementById('prankBanner');
            prankBanner.style.display = 'flex';
            
            // Add some extra fun effects
            setTimeout(() => {
                const prankContent = document.querySelector('.prank-content');
                prankContent.style.transform = 'scale(1.1)';
                setTimeout(() => {
                    prankContent.style.transform = 'scale(1)';
                }, 200);
            }, 300);
        }
        
        function closePrank() {
            const prankBanner = document.getElementById('prankBanner');
            prankBanner.style.animation = 'slideDown 0.5s ease-out reverse';
            
            setTimeout(() => {
                prankBanner.style.display = 'none';
                prankBanner.style.animation = 'slideDown 0.5s ease-out';
                
                // Reset form for another prank
                document.getElementById('registrationForm').reset();
            }, 500);
        }
        
        // Add some hover effects to make it more convincing
        document.getElementById('schoolId').addEventListener('input', function() {
            if (this.value && Number.isInteger(Number(this.value)) && Number(this.value) > 0) {
                this.style.borderColor = '#4ecdc4';
            } else {
                this.style.borderColor = '#e1e5e9';
            }
        });
    </script>
</body>
</html>
