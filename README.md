<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="New Hire.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LHL Employee Management System</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f5f7fa;
        }
        .id-card {
            width: 85mm;
            height: 54mm;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }
        .id-front {
            background: linear-gradient(135deg, #2563eb 0%, #1e40af 100%);
            color: white;
        }
        .id-back {
            background: white;
            color: #333;
        }
        .photo-circle {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            border: 3px solid white;
            overflow: hidden;
        }
        
    </style>
</head>
<body class="bg-gray-100">
    <div class="container mx-auto px-4 py-8">
        <div class="flex justify-between items-center mb-8">
            <h1 class="text-3xl font-bold text-gray-800">LHL Employee Management</h1>
            <div class="flex items-center space-x-4">
                <img src="https://placehold.co/80x50?text=LHL+Logo" alt="LHL Technologies company logo with blue and white colors" class="h-10">
            </div>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
            <!-- Employee Form -->
            <div class="bg-white rounded-lg shadow-lg p-6 no-print">
                <h2 class="text-xl font-semibold mb-4 text-gray-800">Employee Details</h2>
                <form id="employeeForm" class="space-y-4">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Employee Name</label>
                            <input type="text" required id="empName" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Employee ID</label>
                      <input type="text" required id="emp id" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                   
</div>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Employee Photo</label>
                            <div class="flex items-center space-x-4">
                                <img id="photoPreview" src="https://placehold.co/100x100?text=Photo" alt="Employee photo placeholder" class="rounded-full h-16 w-16 object-cover border-2 border-gray-300">
                                <input type="file" id="empPhoto" accept="image/*" class="hidden">
                                <button type="button" onclick="document.getElementById('empPhoto').click()" class="px-3 py-1 bg-blue-500 text-white rounded-md hover:bg-blue-600">Upload</button>
                            </div>
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Department</label>
                            <select id="empDept" required class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option value="">Select Department</option>
                                <option value="IT">IT</option>
                                <option value="HR">HR</option>
                                <option value="Finance">Finance</option>
                                <option value="Marketing">Marketing</option>
                                <option value="Operations">Operations</option>
                                <option value="Sales">Sales</option>
                                <option value="R&D">R&D</option>
                            </select>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Designation</label>
                            <input type="text" required id="empDesignation" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Blood Group</label>
                            <select id="empBloodGroup" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option value="">Select Blood Group</option>
                                <option value="A+">A+</option>
                                <option value="A-">A-</option>
                                <option value="B+">B+</option>
                                <option value="B-">B-</option>
                                <option value="AB+">AB+</option>
                                <option value="AB-">AB-</option>
                                <option value="O+">O+</option>
                                <option value="O-">O-</option>
                            </select>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Mobile Number</label>
                            <input type="tel" required id="empMobile" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Email ID</label>
                            <input type="email" required id="empEmail" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Communication Address</label>
                        <textarea id="empCommAddress" rows="2" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Permanent Address</label>
                        <textarea id="empPermAddress" rows="2" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
                    </div>

                    <div>
                    <div class="pt-4">
                        <button type="submit" class="px-6 py-2 bg-blue-600 text-white rounded-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">Save Employee</button>
                        <button type="button" id="resetForm" class="px-6 py-2 ml-3 bg-gray-200 text-gray-800 rounded-md hover:bg-gray-300 focus:outline-none focus:ring-2 focus:ring-gray-500 focus:ring-offset-2">Reset</button>
                    </div>
                </form>
            </div>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Employee ID Card Generator</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f7fa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .id-card-container {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .id-card {
            width: 350px;
            height: 500px;
            perspective: 1000px;
            margin-bottom: 20px;
        }

        .id-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
            transition: transform 0.8s;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .id-card:hover .id-card-inner {
            transform: rotateY(180deg);
        }

        .id-card-front, .id-card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 15px;
            overflow: hidden;
        }

        .id-card-front {
            background: linear-gradient(135deg, #4a89dc, #5d9cec);
            color: white;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .id-card-back {
            background-color: white;
            transform: rotateY(180deg);
            display: flex;
            flex-direction: column;
            padding: 20px;
            color: #333;
        }

        .company-header {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 15px;
            width: 100%;
        }

        .company-logo {
            width: 50px;
            height: 50px;
            margin-right: 10px;
            background-color: white;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #4a89dc;
            font-size: 20px;
        }

        .company-name {
            font-size: 22px;
            font-weight: 700;
        }

        .employee-photo {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid white;
            margin: 15px 0;
            overflow: hidden;
            background-color: #e0e0e0;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .employee-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .employee-name {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .employee-id {
            font-size: 16px;
            margin-bottom: 15px;
            background-color: rgba(255, 255, 255, 0.2);
            padding: 5px 15px;
            border-radius: 20px;
        }

        .employee-details {
            width: 100%;
            margin-top: 15px;
        }

        .detail-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding-bottom: 8px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }

        .detail-label {
            font-weight: 600;
            font-size: 14px;
            text-align: left;
            flex: 1;
        }

        .detail-value {
            font-size: 14px;
            text-align: right;
            flex: 1;
        }

        .back-header {
            font-size: 18px;
            font-weight: 700;
            color: #4a89dc;
            margin-bottom: 20px;
            text-align: center;
            padding-bottom: 10px;
            border-bottom: 2px solid #4a89dc;
        }

        .company-address {
            font-size: 14px;
            line-height: 1.6;
            margin-bottom: 20px;
            text-align: center;
        }

        .emergency-contact {
            background-color: #f5f7fa;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .emergency-title {
            font-weight: 700;
            margin-bottom: 10px;
            color: #4a89dc;
            text-align: center;
        }

        .emergency-details {
            font-size: 14px;
            line-height: 1.6;
            text-align: center;
        }
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Signature Creator</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            margin: 0;
            padding: 20px;
            background-color: #f5f7fa;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .header h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #7f8c8d;
        }
        
        .signature-container {
            width: 100%;
            max-width: 800px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 20px;
        }
        
        .canvas-wrapper {
            position: relative;
            width: 100%;
            height: 200px;
            border: 1px dashed #ccc;
            margin-bottom: 20px;
        }
        
        #signatureCanvas {
            width: 100%;
            height: 100%;
            background-color: #fff;
            cursor: crosshair;
        }
        
        .tools {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .color-picker, .pen-size {
            display: flex;
            align-items: center;
        }
        
        .color-picker label, .pen-size label {
            margin-right: 10px;
            color: #2c3e50;
            font-weight: 500;
        }
        
        #penColor {
            width: 40px;
            height: 40px;
            border: none;
            cursor: pointer;
        }
        
        #penSize {
            width: 80px;
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .clear-btn {
            background-color: #e74c3c;
            color: white;
        }
        
        .clear-btn:hover {
            background-color: #c0392b;
        }
        
        .save-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .save-btn:hover {
            background-color: #27ae60;
        }
        
        .upload-btn {
            background-color: #3498db;
            color: white;
        }
        
        .upload-btn:hover {
            background-color: #2980b9;
        }
        
        .instructions {
            margin-top: 30px;
            background-color: #e8f4f8;
            padding: 15px;
            border-radius: 8px;
            color: #2c3e50;
            width: 100%;
            max-width: 800px;
        }
        
        .instructions h3 {
            margin-top: 0;
            color: #3498db;
        }
        
        .file-input {
            display: none;
        }
        
        .placeholder-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #bdc3c7;
            pointer-events: none;
        }
        
        @media (max-width: 600px) {
            .tools {
                flex-direction: column;
            }
            
            .action-buttons {
                flex-direction: column;
            }
            
            button {
                width: 100%;
            }
        }
    </style>
<br><br><br>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Signature Creator</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            margin: 0;
            padding: 20px;
            background-color: #f5f7fa;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .header h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #7f8c8d;
        }
        
        .signature-container {
            width: 100%;
            max-width: 800px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 20px;
        }
        
        .canvas-wrapper {
            position: relative;
            width: 100%;
            height: 200px;
            border: 1px dashed #ccc;
            margin-bottom: 20px;
        }
        
        #signatureCanvas {
            width: 100%;
            height: 100%;
            background-color: #fff;
            cursor: crosshair;
        }
        
        .tools {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .color-picker, .pen-size {
            display: flex;
            align-items: center;
        }
        
        .color-picker label, .pen-size label {
            margin-right: 10px;
            color: #2c3e50;
            font-weight: 500;
        }
        
        #penColor {
            width: 40px;
            height: 40px;
            border: none;
            cursor: pointer;
        }
        
        #penSize {
            width: 80px;
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .clear-btn {
            background-color: #e74c3c;
            color: white;
        }
        
        .clear-btn:hover {
            background-color: #c0392b;
        }
        
        .save-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .save-btn:hover {
            background-color: #27ae60;
        }
        
        .upload-btn {
            background-color: #3498db;
            color: white;
        }
        
        .upload-btn:hover {
            background-color: #2980b9;
        }
        
        .instructions {
            margin-top: 30px;
            background-color: #e8f4f8;
            padding: 15px;
            border-radius: 8px;
            color: #2c3e50;
            width: 100%;
            max-width: 800px;
        }
        
        .instructions h3 {
            margin-top: 0;
            color: #3498db;
        }
        
        .file-input {
            display: none;
        }
        
        .placeholder-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #bdc3c7;
            pointer-events: none;
        }
        
        @media (max-width: 600px) {
            .tools {
                flex-direction: column;
            }
            
            .action-buttons {
                flex-direction: column;
            }
            
            button {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Digital Signature Creator</h1>
        <p>Create or upload your digital signature</p>
    </div>
    
    <div class="signature-container">
        <div class="canvas-wrapper">
            <canvas id="signatureCanvas"></canvas>
            <div class="placeholder-text">Draw your signature here</div>
        </div>
        
        <div class="tools">
            <div class="color-picker">
                <label for="penColor">Pen Color:</label>
                <input type="color" id="penColor" value="#000000">
            </div>
            
            <div class="pen-size">
                <label for="penSize">Pen Size:</label>
                <input type="range" id="penSize" min="1" max="10" value="2">
            </div>
        </div>
        
        <div class="action-buttons">
            <button class="clear-btn" id="clearBtn">Clear Signature</button>
            <button class="save-btn" id="saveBtn">Save Signature</button>
            <button class="upload-btn" id="uploadBtn">Upload Signature</button>
            <input type="file" id="fileInput" class="file-input" accept="image/*">
        </div>
    </div>
   </div>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const canvas = document.getElementById('signatureCanvas');
            const ctx = canvas.getContext('2d');
            const placeholderText = document.querySelector('.placeholder-text');
            const penColor = document.getElementById('penColor');
            const penSize = document.getElementById('penSize');
            const clearBtn = document.getElementById('clearBtn');
            const saveBtn = document.getElementById('saveBtn');
            const uploadBtn = document.getElementById('uploadBtn');
            const fileInput = document.getElementById('fileInput');
            
            let isDrawing = false;
            let lastX = 0;
            let lastY = 0;
            
            // Set canvas size
            function resizeCanvas() {
                const rect = canvas.parentElement.getBoundingClientRect();
                canvas.width = rect.width;
                canvas.height = rect.height;
                canvas.style.width = rect.width + 'px';
                canvas.style.height = rect.height + 'px';
            }
            
            // Initial resize
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // Drawing functions
            function startDrawing(e) {
                isDrawing = true;
                [lastX, lastY] = getCoordinates(e);
                placeholderText.style.display = 'none';
            }
            
            function draw(e) {
                if (!isDrawing) return;
                
                ctx.strokeStyle = penColor.value;
                ctx.lineWidth = penSize.value;
                ctx.lineJoin = 'round';
                ctx.lineCap = 'round';
                
                const [x, y] = getCoordinates(e);
                
                ctx.beginPath();
                ctx.moveTo(lastX, lastY);
                ctx.lineTo(x, y);
                ctx.stroke();
                
                [lastX, lastY] = [x, y];
            }
            
            function stopDrawing() {
                isDrawing = false;
            }
            
            function getCoordinates(e) {
                let x, y;
                if (e.type.includes('touch')) {
                    x = e.touches[0].clientX - canvas.getBoundingClientRect().left;
                    y = e.touches[0].clientY - canvas.getBoundingClientRect().top;
                } else {
                    x = e.offsetX;
                    y = e.offsetY;
                }
                return [x, y];
            }
            
            // Event listeners for drawing
            canvas.addEventListener('mousedown', startDrawing);
            canvas.addEventListener('mousemove', draw);
            canvas.addEventListener('mouseup', stopDrawing);
            canvas.addEventListener('mouseout', stopDrawing);
            
            // Touch support
            canvas.addEventListener('touchstart', function(e) {
                e.preventDefault();
                startDrawing(e);
            });
            
            canvas.addEventListener('touchmove', function(e) {
                e.preventDefault();
                draw(e);
            });
            
            canvas.addEventListener('touchend', stopDrawing);
            
            // Clear canvas
            clearBtn.addEventListener('click', function() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                placeholderText.style.display = 'block';
            });
            
            // Save signature
            saveBtn.addEventListener('click', function() {
                if (isCanvasEmpty(canvas)) {
                    alert('Please create a signature first');
                    return;
                }
                
                const link = document.createElement('a');
                link.download = 'signature.png';
                link.href = canvas.toDataURL('image/png');
                link.click();
            });
            
            // Upload signature
            uploadBtn.addEventListener('click', function() {
                fileInput.click();
            });
            
            fileInput.addEventListener('change', function(e) {
                if (e.target.files && e.target.files[0]) {
                    const reader = new FileReader();
                    
                    reader.onload = function(event) {
                        const img = new Image();
                        img.onload = function() {
                            // Clear canvas
                            ctx.clearRect(0, 0, canvas.width, canvas.height);
                            placeholderText.style.display = 'none';
                            
                            // Calculate dimensions to fit the canvas while maintaining aspect ratio
                            const scale = Math.min(
                                canvas.width / img.width,
                                canvas.height / img.height
                            );
                            const width = img.width * scale;
                            const height = img.height * scale;
                            const x = (canvas.width - width) / 2;
                            const y = (canvas.height - height) / 2;
                            
                            // Draw the image
                            ctx.drawImage(img, x, y, width, height);
                        };
                        img.src = event.target.result;
                    };
                    
                    reader.readAsDataURL(e.target.files[0]);
                }
            });
            
            // Check if canvas is empty
            function isCanvasEmpty(canvas) {
                const blank = document.createElement('canvas');
                blank.width = canvas.width;
                blank.height = canvas.height;
                return canvas.toDataURL() === blank.toDataURL();
            }
        });
    </script>
</body>
</html>
    </style>
</head>
<body>
    <div class="id-card-container">
        <div class="id-card">
            <div class="id-card-inner">
                <div class="id-card-front">
                    <div class="company-header">
                        <div class="company-logo">LHL</div>
                        <div class="company-name">Lighthouse Labs</div>
                    </div>
                    
                    <div class="employee-photo">
                        <img src="https://placehold.co/400x400" alt="Professional headshot of employee with neutral background" />
                    </div>
                    
                    <div class="employee-name">John Doe</div>
                    <div class="employee-id">LHL00456</div>
                    
                    <div class="employee-details">
                        <div class="detail-row">
                            <div class="detail-label">Department:</div>
                            <div class="detail-value">Information Technology</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Designation:</div>
                            <div class="detail-value">Senior Developer</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Mobile:</div>
                            <div class="detail-value">+91 9876543210</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Date of Joining:</div>
                            <div class="detail-value">15 Jan 2020</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Blood Group:</div>
                            <div class="detail-value">B+</div>
                        </div>
                    </div>
                </div>
                
                <div class="id-card-back">
                    <div class="back-header">Lighthouse Labs</div>
                    
                    <div class="company-address">
                        123 Tech Park, Sector 12<br>
                        Cyber City, Gurgaon<br>
                        Haryana - 122001, India<br>
                        www.lighthouselabs.com
                    </div>
                    
                    <div class="emergency-contact">
                        <div class="emergency-title">In Case of Emergency</div>
                        <div class="emergency-details">
                            Contact HR Department<br>
                            Phone: +91 124 4567890<br>
                            Email: hr@lighthouselabs.com
                        </div>
                    </div>
                    
                    <div class="signature-area">
                        <div class="signature-line"></div>
                        <div class="signature-label">Authorized Signature</div>
                    </div>
                    
                    <div class="validity">Valid until: 31 Dec 2024</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const departments = [
            "Information Technology",
            "Human Resources",
            "Finance",
            "Marketing",
            "Operations",
            "Sales",
            "Customer Support",
            "Research & Development"
        ];

        const designations = {
            "Information Technology": ["Junior Developer", "Developer", "Senior Developer", "Tech Lead", "Manager"],
            "Human Resources": ["HR Associate", "HR Manager", "HR Director"],
            "Finance": ["Accountant", "Financial Analyst", "Finance Manager"],
            "Marketing": ["Marketing Associate", "Marketing Manager"],
            "Operations": ["Operations Executive", "Operations Manager"],
            "Sales": ["Sales Executive", "Sales Manager"],
            "Customer Support": ["Support Executive", "Support Manager"],
            "Research & Development": ["Research Associate", "Research Scientist"]
        };

        const bloodGroups = ["A+", "A-", "B+", "B-", "AB+", "AB-", "O+", "O-"];

        function generateEmployeeCard() {
            // Generate random employee details
            const firstName = getRandomName();
            const lastName = getRandomName();
            const empName = `${firstName} ${lastName}`;
            
            // Generate employee ID in format LHLXXXXX (XXXXX from 00001 to 10000)
            const empIdNum = Math.floor(Math.random() * 10000) + 1;
            const empId = `LHL${empIdNum.toString().padStart(5, '0')}`;
            
            const department = departments[Math.floor(Math.random() * departments.length)];
            const designation = designations[department][Math.floor(Math.random() * designations[department].length)];
            
            // Generate random phone number
            const mobileNumber = `+91 ${Math.floor(1000000000 + Math.random() * 9000000000).toString().substring(1, 11)}`;
            
            // Generate random date of joining (between 2015 and 2023)
            const joinYear = Math.floor(Math.random() * 9) + 2015;
            const joinMonth = Math.floor(Math.random() * 12);
            const joinDay = Math.floor(Math.random() * 28) + 1;
            const joinDate = new Date(joinYear, joinMonth, joinDay);
            const options = { day: '2-digit', month: 'short', year: 'numeric' };
            const formattedDate = joinDate.toLocaleDateString('en-US', options);
            
            const bloodGroup = bloodGroups[Math.floor(Math.random() * bloodGroups.length)];
            
            // Generate random photo placeholder with different dimensions
            const photoWidth = Math.floor(Math.random() * 200) + 400;
            const photoHeight = photoWidth; // Keep it square
            
            // Update the DOM elements
            document.querySelector('.employee-name').textContent = empName;
            document.querySelector('.employee-id').textContent = empId;
            document.querySelector('.employee-photo img').src = `https://placehold.co/${photoWidth}x${photoHeight}`;
            document.querySelector('.employee-photo img').alt = `Professional headshot of ${empName}`;
            
            const detailRows = document.querySelectorAll('.detail-row');
            detailRows[0].querySelector('.detail-value').textContent = department;
            detailRows[1].querySelector('.detail-value').textContent = designation;
            detailRows[2].querySelector('.detail-value').textContent = mobileNumber;
            detailRows[3].querySelector('.detail-value').textContent = formattedDate;
            detailRows[4].querySelector('.detail-value').textContent = bloodGroup;
            
            // Generate random validity date
            const validityYear = joinYear + Math.floor(Math.random() * 5) + 1;
            document.querySelector('.validity').textContent = `Valid until: 31 Dec ${validityYear}`;
        }

        function getRandomName() {
            const names = [
                "Aarav", "Aditi", "Arjun", "Avni", "Dev", "Dhruv", "Diya", "Ishaan",
                "Kavya", "Kiara", "Mohit", "Neha", "Parth", "Prisha", "Reyansh", "Riya",
                "Shaurya", "Siya", "Soham", "Tanvi", "Ved", "Yash", "Zara",
                "John", "Michael", "David", "Sarah", "Jennifer", "Robert", "Emily", "Daniel",
                "Lisa", "William", "Jessica", "Christopher", "Ashley", "Matthew", "Amanda",
                "James", "Elizabeth", "Andrew", "Nicole", "Ryan", "Stephanie"
            ];
            return names[Math.floor(Math.random() * names.length)];
        }

        // Generate an initial card when page loads
        window.onload = function() {
            generateEmployeeCard();
        };
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="logo.jpg"="https://place.c/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="New hire.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header>
        <!-- Main Content -->
        <main class="flex-grow container mx-auto px-4 py-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Welcome to HR Dashboard</h2>
                <p class="text-xl text-gray-600 max-w-3xl mx-auto">Streamline your HR processes with our comprehensive dashboard solution</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Employee management Card -->
               <a href="employee management.html" class="card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="p-6">
                        <div class="flex justify-center mb-4">
                            <div class="bg-red-100 p-3 rounded-full">
                                <img src="https://placehold.co/50x50" alt="Icon representing employee all data and record  with document and exit door symbol" class="w-50 h-50">
                            </div>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-1500 mb-2">Employee management</h3>
                        <p class="text-gray-3000">View and manage employee data and record</p>
                    </div>
                   </a>
                <!-- Salary Card -->
                <a href="salary.html" class="card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="p-6">
                        <div class="flex justify-center mb-4">
                            <div class="bg-green-100 p-3 rounded-full">
                                <img src="https://placehold.co/50x50" alt="Icon representing financial documents with dollar sign symbol" class="w-12 h-12">
                            </div>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-800 mb-2">Salary</h3>
                        <p class="text-gray-600">Generate and manage employee payroll records</p>
                    </div>
                </a>
                <!-- Attendance Card -->
                <a href="Attandance.html" class="card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="p-6">
                        <div class="flex justify-center mb-4">
                            <div class="bg-yellow-100 p-3 rounded-full">
                                <img src="https://placehold.co/50x50" alt="Icon representing attendance clock with check-in/check-out symbols" class="w-12 h-12">
                            </div>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-800 mb-2">Attandance</h3>
                        <p class="text-gray-600">Track employee attendance and working hours</p>
                    </div>
                </a>
                <!-- Leave Card -->
                <a href="leave.html" class="card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="p-6">
                        <div class="flex justify-center mb-4">
                            <div class="bg-purple-100 p-3 rounded-full">
                                <img src="https://placehold.co/50x50" alt="Icon representing vacation time with beach umbrella and palm tree" class="w-12 h-12">
                            </div>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-800 mb-2">Leave Tracker</h3>
                        <p class="text-gray-600">Manage employee leave requests and approvals</p>
                    </div>
                </a>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mt-8">
                <!-- Terminate Employee List Card -->
                <a href="resignations.html" class="card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="p-6">
                        <div class="flex justify-center mb-4">
                            <div class="bg-red-100 p-3 rounded-full">
                                <img src="https://placehold.co/50x50" alt="Icon representing employee Termination with document and exit door symbol" class="w-12 h-12">
                            </div>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-800 mb-2">Termination Latter</h3>
                        <p class="text-gray-600">View and manage employee Termination</p>
                    </div>
                </a>

                <!-- Reports Card -->
                <a href="reports.html" class="card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="p-6">
                        <div class="flex justify-center mb-4">
                            <div class="bg-indigo-100 p-3 rounded-full">
                                <img src="https://placehold.co/50x50" alt="Icon representing analytics reports with bar chart and pie chart symbols" class="w-12 h-12">
                            </div>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-800 mb-2">Reports</h3>
                        <p class="text-gray-600">Generate HR analytics and reports</p>
                    </div>
                </a>

                <!-- Contact Card -->
                <a href="contacts.html" class="card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="p-6">
                        <div class="flex justify-center mb-4">
                            <div class="bg-pink-100 p-3 rounded-full">
                                <img src="https://placehold.co/50x50" alt="Icon representing contact information with phone and email symbols" class="w-12 h-12">
                            </div>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-800 mb-2">Contacts</h3>
                        <p class="text-gray-600">Contact information and support</p>
                    </div>
                </a>
            </div>
        </main>

        <!-- Footer -->
        <footer class="bg-gray-800 text-white py-8">
            <div class="container mx-auto px-4">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <div class="mb-4 md:mb-0">
                        <h3 class="text-xl font-bold mb-2">HR Dashboard</h3>
                        <p class="text-gray-400">© 2023 Company Name. All rights reserved.</p>
                    </div>
                    <nav>
                        <ul class="flex space-x-6">
                            <li><a href="index.html" class="hover:text-blue-400">Home</a></li>
                            <li><a href="privacy.html" class="hover:text-blue-400">Privacy Policy</a></li>
                            <li><a href="terms.html" class="hover:text-blue-400">Terms</a></li>
                            <li><a href="contact.html" class="hover:text-blue-400">Contact</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </footer>
    </div>
</body>
</html>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Employee ID Card Generator</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f7fa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .id-card-container {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .id-card {
            width: 350px;
            height: 500px;
            perspective: 1000px;
            margin-bottom: 20px;
        }

        .id-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
            transition: transform 0.8s;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .id-card:hover .id-card-inner {
            transform: rotateY(180deg);
        }

        .id-card-front, .id-card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 15px;
            overflow: hidden;
        }

        .id-card-front {
            background: linear-gradient(135deg, #4a89dc, #5d9cec);
            color: white;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .id-card-back {
            background-color: white;
            transform: rotateY(180deg);
            display: flex;
            flex-direction: column;
            padding: 20px;
            color: #333;
        }

        .company-header {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 15px;
            width: 100%;
        }

        .company-logo {
            width: 50px;
            height: 50px;
            margin-right: 10px;
            background-color: white;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #4a89dc;
            font-size: 20px;
        }

        .company-name {
            font-size: 22px;
            font-weight: 700;
        }

        .employee-photo {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid white;
            margin: 15px 0;
            overflow: hidden;
            background-color: #e0e0e0;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .employee-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .employee-name {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .employee-id {
            font-size: 16px;
            margin-bottom: 15px;
            background-color: rgba(255, 255, 255, 0.2);
            padding: 5px 15px;
            border-radius: 20px;
        }

        .employee-details {
            width: 100%;
            margin-top: 15px;
        }

        .detail-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding-bottom: 8px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }

        .detail-label {
            font-weight: 600;
            font-size: 14px;
            text-align: left;
            flex: 1;
        }

        .detail-value {
            font-size: 14px;
            text-align: right;
            flex: 1;
        }

        .back-header {
            font-size: 18px;
            font-weight: 700;
            color: #4a89dc;
            margin-bottom: 20px;
            text-align: center;
            padding-bottom: 10px;
            border-bottom: 2px solid #4a89dc;
        }

        .company-address {
            font-size: 14px;
            line-height: 1.6;
            margin-bottom: 20px;
            text-align: center;
        }

        .emergency-contact {
            background-color: #f5f7fa;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .emergency-title {
            font-weight: 700;
            margin-bottom: 10px;
            color: #4a89dc;
            text-align: center;
        }

        .emergency-details {
            font-size: 14px;
            line-height: 1.6;
            text-align: center;
        }

        .signature-area {
            margin-top: auto;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .signature-line {
            width: 60%;
            border-top: 1px solid #333;
            margin-top: 30px;
            position: relative;
        }

        .signature-label {
            font-size: 12px;
            margin-top: 5px;
        }

        .validity {
            font-size: 10px;
            text-align: center;
            margin-top: 10px;
            opacity: 0.7;
        }

        .controls {
            margin-top: 30px;
            text-align: center;
            width: 100%;
        }

        button {
            background-color: #4a89dc;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            margin: 0 10px;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #3b7dd8;
        }

        @media (max-width: 768px) {
            .id-card {
                width: 100%;
                max-width: 350px;
            }
        }
    </style>
</head>
<body>
    <div class="id-card-container">
        <div class="id-card">
            <div class="id-card-inner">
                <div class="id-card-front">
                    <div class="company-header">
                        <div class="company-logo">LHL</div>
                        <div class="company-name">Lighthouse Labs</div>
                    </div>
                    
                    <div class="employee-photo">
                        <img src="https://placehold.co/400x400" alt="Professional headshot of employee with neutral background" />
                    </div>
                    
                    <div class="employee-name">John Doe</div>
                    <div class="employee-id">LHL00456</div>
                    
                    <div class="employee-details">
                        <div class="detail-row">
                            <div class="detail-label">Department:</div>
                            <div class="detail-value">Information Technology</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Designation:</div>
                            <div class="detail-value">Senior Developer</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Mobile:</div>
                            <div class="detail-value">+91 9876543210</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Date of Joining:</div>
                            <div class="detail-value">15 Jan 2020</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Blood Group:</div>
                            <div class="detail-value">B+</div>
                        </div>
                    </div>
                </div>
                
                <div class="id-card-back">
                    <div class="back-header">Lighthouse Labs</div>
                    
                    <div class="company-address">
                        123 Tech Park, Sector 12<br>
                        Cyber City, Gurgaon<br>
                        Haryana - 122001, India<br>
                        www.lighthouselabs.com
                    </div>
                    
                    <div class="emergency-contact">
                        <div class="emergency-title">In Case of Emergency</div>
                        <div class="emergency-details">
                            Contact HR Department<br>
                            Phone: +91 124 4567890<br>
                            Email: hr@lighthouselabs.com
                        </div>
                    </div>
                    
                    <div class="signature-area">
                        <div class="signature-line"></div>
                        <div class="signature-label">Authorized Signature</div>
                    </div>
                    
                    <div class="validity">Valid until: 31 Dec 2024</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const departments = [
            "Information Technology",
            "Human Resources",
            "Finance",
            "Marketing",
            "Operations",
            "Sales",
            "Customer Support",
            "Research & Development"
        ];

        const designations = {
            "Information Technology": ["Junior Developer", "Developer", "Senior Developer", "Tech Lead", "Manager"],
            "Human Resources": ["HR Associate", "HR Manager", "HR Director"],
            "Finance": ["Accountant", "Financial Analyst", "Finance Manager"],
            "Marketing": ["Marketing Associate", "Marketing Manager"],
            "Operations": ["Operations Executive", "Operations Manager"],
            "Sales": ["Sales Executive", "Sales Manager"],
            "Customer Support": ["Support Executive", "Support Manager"],
            "Research & Development": ["Research Associate", "Research Scientist"]
        };

        const bloodGroups = ["A+", "A-", "B+", "B-", "AB+", "AB-", "O+", "O-"];

        function generateEmployeeCard() {
            // Generate random employee details
            const firstName = getRandomName();
            const lastName = getRandomName();
            const empName = `${firstName} ${lastName}`;
            
            // Generate employee ID in format LHLXXXXX (XXXXX from 00001 to 10000)
            const empIdNum = Math.floor(Math.random() * 10000) + 1;
            const empId = `LHL${empIdNum.toString().padStart(5, '0')}`;
            
            const department = departments[Math.floor(Math.random() * departments.length)];
            const designation = designations[department][Math.floor(Math.random() * designations[department].length)];
            
            // Generate random phone number
            const mobileNumber = `+91 ${Math.floor(1000000000 + Math.random() * 9000000000).toString().substring(1, 11)}`;
            
            // Generate random date of joining (between 2015 and 2023)
            const joinYear = Math.floor(Math.random() * 9) + 2015;
            const joinMonth = Math.floor(Math.random() * 12);
            const joinDay = Math.floor(Math.random() * 28) + 1;
            const joinDate = new Date(joinYear, joinMonth, joinDay);
            const options = { day: '2-digit', month: 'short', year: 'numeric' };
            const formattedDate = joinDate.toLocaleDateString('en-US', options);
            
            const bloodGroup = bloodGroups[Math.floor(Math.random() * bloodGroups.length)];
            
            // Generate random photo placeholder with different dimensions
            const photoWidth = Math.floor(Math.random() * 200) + 400;
            const photoHeight = photoWidth; // Keep it square
            
            // Update the DOM elements
            document.querySelector('.employee-name').textContent = empName;
            document.querySelector('.employee-id').textContent = empId;
            document.querySelector('.employee-photo img').src = `https://placehold.co/${photoWidth}x${photoHeight}`;
            document.querySelector('.employee-photo img').alt = `Professional headshot of ${empName}`;
            
            const detailRows = document.querySelectorAll('.detail-row');
            detailRows[0].querySelector('.detail-value').textContent = department;
            detailRows[1].querySelector('.detail-value').textContent = designation;
            detailRows[2].querySelector('.detail-value').textContent = mobileNumber;
            detailRows[3].querySelector('.detail-value').textContent = formattedDate;
            detailRows[4].querySelector('.detail-value').textContent = bloodGroup;
            
            // Generate random validity date
            const validityYear = joinYear + Math.floor(Math.random() * 5) + 1;
            document.querySelector('.validity').textContent = `Valid until: 31 Dec ${validityYear}`;
        }

        function getRandomName() {
            const names = [
                "Aarav", "Aditi", "Arjun", "Avni", "Dev", "Dhruv", "Diya", "Ishaan",
                "Kavya", "Kiara", "Mohit", "Neha", "Parth", "Prisha", "Reyansh", "Riya",
                "Shaurya", "Siya", "Soham", "Tanvi", "Ved", "Yash", "Zara",
                "John", "Michael", "David", "Sarah", "Jennifer", "Robert", "Emily", "Daniel",
                "Lisa", "William", "Jessica", "Christopher", "Ashley", "Matthew", "Amanda",
                "James", "Elizabeth", "Andrew", "Nicole", "Ryan", "Stephanie"
            ];
            return names[Math.floor(Math.random() * names.length)];
        }

        // Generate an initial card when page loads
        window.onload = function() {
            generateEmployeeCard();
        };
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Employee Leave Management Portal</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom styles */
        .leave-card {
            transition: all 0.3s ease;
        }
        .leave-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .status-pending {
            border-left: 4px solid #F59E0B;
        }
        .status-approved {
            border-left: 4px solid #10B981;
        }
        .status-rejected {
            border-left: 4px solid #EF4444;
        }
        .status-hold {
            border-left: 4px solid #3B82F6;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header -->
    <header class="bg-blue-600 text-white shadow-md">
        <div class="container mx-auto px-4 py-6">
            <div class="flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/40x40" alt="Company logo featuring a stylized letter 'A' in blue and white" class="rounded-full">
                    <h1 class="text-2xl font-bold">Employee Leave Portal</h1>
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="New Hire.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
    <meta charset="UTF-8">
                </div>
                <div class="hidden md:block">
                    <p class="text-blue-100">Welcome, <span class="font-semibold text-white">Admin</span></p>
                </div>
            </div>
        </div>
    </header>
        <!-- Main Content -->
    <main class="container mx-auto px-4 py-8">
        <!-- Leave Request Form -->
        <section class="bg-white rounded-lg shadow-md p-6 mb-8">
            <h2 class="text-xl font-semibold text-gray-800 mb-4">Request New Leave</h2>
            <form id="leaveForm" class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <!-- Employee Info -->
                <div class="col-span-2 grid grid-cols-1 md:grid-cols-3 gap-4 border-b pb-4 mb-2">
                    <div>
                        <label for="empName" class="block text-sm font-medium text-gray-700 mb-1">Employee Name</label>
                        <input type="text" id="empName" name="empName" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                    </div>
                    <div>
                        <label for="empId" class="block text-sm font-medium text-gray-700 mb-1">Employee ID</label>
                        <input type="text" id="empId" name="empId" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                    </div>
                    <div>
                        <label for="empMobile" class="block text-sm font-medium text-gray-700 mb-1">Mobile Number</label>
                        <input type="tel" id="empMobile" name="empMobile" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                    </div>
                    <div>
                        <label for="empDesignation" class="block text-sm font-medium text-gray-700 mb-1">Designation</label>
                        <input type="text" id="empDesignation" name="empDesignation" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                    </div>
                    <div>
                        <label for="empDepartment" class="block text-sm font-medium text-gray-700 mb-1">Department</label>
                        <select id="empDepartment" name="empDepartment" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                            <option value="">Select Department</option>
                            <option value="HR">Human Resources</option>
                            <option value="IT">Information Technology</option>
                            <option value="Finance">Finance</option>
                            <option value="Marketing">Marketing</option>
                            <option value="Operations">Operations</option>
                        </select>
                    </div>
                    <div>
                        <label for="empCode" class="block text-sm font-medium text-gray-700 mb-1">E-mail id</label>
                        <input type="text" id="empCode" name="empCode" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                    </div>
                </div>

                <!-- Leave Details -->
                <div>
                    <label for="leaveType" class="block text-sm font-medium text-gray-700 mb-1">Leave Type</label>
                    <select id="leaveType" name="leaveType" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                        <option value="">Select Leave Type</option>
                        <option value="sick">Sick Leave</option>
                        <option value="casual">Casual Leave</option>
                        <option value="religious">Religious Holiday</option>
                        <option value="national">National Holiday</option>
                    </select>
                </div>

                <div>
                    <label for="startDate" class="block text-sm font-medium text-gray-700 mb-1">Start Date</label>
                    <input type="date" id="startDate" name="startDate" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                </div>

                <div>
                    <label for="endDate" class="block text-sm font-medium text-gray-700 mb-1">End Date</label>
                    <input type="date" id="endDate" name="endDate" required class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                </div>

                <div class="md:col-span-2">
                    <label for="leaveReason" class="block text-sm font-medium text-gray-700 mb-1">Reason for Leave</label>
                    <textarea id="leaveReason" name="leaveReason" rows="3" class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500"></textarea>
                </div>

                <div class="md:col-span-2 flex justify-end">
                    <button type="submit" class="px-4 py-2 bg-blue-600 text-white rounded-md shadow-sm hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
                        Submit Leave Request
                    </button>
                </div>
            </form>
        </section>

        <!-- Admin Panel -->
        <section class="bg-white rounded-lg shadow-md p-6">
            <h2 class="text-xl font-semibold text-gray-800 mb-6">Leave Requests</h2>
            
            <!-- Filters -->
            <div class="flex flex-wrap gap-4 mb-6">
                <div class="flex-1">
                    <label for="filterStatus" class="block text-sm font-medium text-gray-700 mb-1">Filter by Status</label>
                    <select id="filterStatus" class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                        <option value="all">All Statuses</option>
                        <option value="pending">Pending</option>
                        <option value="approved">Approved</option>
                        <option value="rejected">Rejected</option>
                        <option value="hold">On Hold</option>
                    </select>
                </div>
                <div class="flex-1">
                    <label for="filterDepartment" class="block text-sm font-medium text-gray-700 mb-1">Filter by Department</label>
                    <select id="filterDepartment" class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                        <option value="all">All Departments</option>
                        <option value="HR">HR</option>
                        <option value="IT">IT</option>
                        <option value="Finance">Finance</option>
                        <option value="Marketing">Marketing</option>
                        <option value="Operations">Operations</option>
                    </select>
                </div>
                <div class="flex items-end">
                    <button id="applyFilters" class="px-4 py-2 bg-blue-600 text-white rounded-md shadow-sm hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
                        Apply Filters
                    </button>
                </div>
            </div>

            <!-- Leave Requests Listing -->
            <div id="leaveRequests" class="space-y-4">
                <!-- Sample leave request cards - these would be generated dynamically -->
                <div class="leave-card status-pending bg-white p-4 rounded-lg shadow-sm border-l-4">
                    <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4">
                        <div>
                            <h3 class="font-medium text-gray-800">John Doe (ID: EMP1024)</h3>
                            <p class="text-sm text-gray-500">IT Department • Software Engineer</p>
                            <div class="mt-2 flex flex-wrap gap-4">
                                <span class="text-sm"><span class="font-medium">Type:</span> Sick Leave</span>
                                <span class="text-sm"><span class="font-medium">Dates:</span> 15-18 Nov 2023</span>
                                <span class="text-sm"><span class="font-medium">Reason:</span> High fever and flu</span>
                            </div>
                        </div>
                        <div class="flex space-x-2">
                            <button class="approve-btn px-3 py-1 bg-green-500 text-white text-xs rounded hover:bg-green-600" data-id="1">
                                Approve
                            </button>
                            <button class="reject-btn px-3 py-1 bg-red-500 text-white text-xs rounded hover:bg-red-600" data-id="1">
                                Reject
                            </button>
                            <button class="hold-btn px-3 py-1 bg-blue-500 text-white text-xs rounded hover:bg-blue-600" data-id="1">
                                Hold
                            </button>
                        </div>
                    </div>
                </div>

                <div class="leave-card status-approved bg-white p-4 rounded-lg shadow-sm border-l-4">
                    <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4">
                        <div>
                            <h3 class="font-medium text-gray-800">Jane Smith (ID: EMP2048)</h3>
                            <p class="text-sm text-gray-500">HR Department • HR Manager</p>
                            <div class="mt-2 flex flex-wrap gap-4">
                                <span class="text-sm"><span class="font-medium">Type:</span> Religious Holiday</span>
                                <span class="text-sm"><span class="font-medium">Dates:</span> 12 Nov 2023</span>
                                <span class="text-sm"><span class="font-medium">Reason:</span> Diwali celebration</span>
                            </div>
                        </div>
                        <div class="text-green-600 font-medium text-sm">
                            Approved
                        </div>
                    </div>
                </div>

                <div class="leave-card status-rejected bg-white p-4 rounded-lg shadow-sm border-l-4">
                    <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4">
                        <div>
                            <h3 class="font-medium text-gray-800">Mike Johnson (ID: EMP3072)</h3>
                            <p class="text-sm text-gray-500">Marketing Department • Content Specialist</p>
                            <div class="mt-2 flex flex-wrap gap-4">
                                <span class="text-sm"><span class="font-medium">Type:</span> Casual Leave</span>
                                <span class="text-sm"><span class="font-medium">Dates:</span> 20-23 Nov 2023</span>
                                <span class="text-sm"><span class="font-medium">Reason:</span> Family vacation</span>
                            </div>
                        </div>
                        <div class="text-red-600 font-medium text-sm">
                            Rejected (Insufficient leave balance)
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Form submission
            const leaveForm = document.getElementById('leaveForm');
            const leaveRequests = document.getElementById('leaveRequests');
            
            // Sample data - in a real app, this would come from a database
            let requests = [
                {
                    id: 1,
                    name: 'John Doe',
                    empId: 'EMP1024',
                    department: 'IT',
                    designation: 'Software Engineer',
                    type: 'sick',
                    startDate: '2023-11-15',
                    endDate: '2023-11-18',
                    reason: 'High fever and flu',
                    status: 'pending'
                },
                {
                    id: 2,
                    name: 'Jane Smith',
                    empId: 'EMP2048',
                    department: 'HR',
                    designation: 'HR Manager',
                    type: 'religious',
                    startDate: '2023-11-12',
                    endDate: '2023-11-12',
                    reason: 'Diwali celebration',
                    status: 'approved'
                },
                {
                    id: 3,
                    name: 'Mike Johnson',
                    empId: 'EMP3072',
                    department: 'Marketing',
                    designation: 'Content Specialist',
                    type: 'casual',
                    startDate: '2023-11-20',
                    endDate: '2023-11-23',
                    reason: 'Family vacation',
                    status: 'rejected',
                    rejectionReason: 'Insufficient leave balance'
                }
            ];

            // Form submission handler
            leaveForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Get form values
                const formData = new FormData(leaveForm);
                const request = {
                    id: Date.now(), // Using timestamp as a simple ID
                    name: formData.get('empName'),
                    empId: formData.get('empId'),
                    department: formData.get('empDepartment'),
                    designation: formData.get('empDesignation'),
                    type: formData.get('leaveType'),
                    startDate: formData.get('startDate'),
                    endDate: formData.get('endDate'),
                    reason: formData.get('leaveReason'),
                    status: 'pending'
                };

                // Add to requests array
                requests.unshift(request);
                
                // Update the UI
                renderLeaveRequests();
                
                // Reset form
                leaveForm.reset();
                
                // Show success message
                alert('Leave request submitted successfully!');
            });

            // Admin action handlers (approve/reject/hold)
            leaveRequests.addEventListener('click', function(e) {
                if (e.target.classList.contains('approve-btn')) {
                    const id = parseInt(e.target.getAttribute('data-id'));
                    updateRequestStatus(id, 'approved');
                } else if (e.target.classList.contains('reject-btn')) {
                    const id = parseInt(e.target.getAttribute('data-id'));
                    const reason = prompt('Please enter rejection reason:');
                    if (reason) {
                        updateRequestStatus(id, 'rejected', reason);
                    }
                } else if (e.target.classList.contains('hold-btn')) {
                    const id = parseInt(e.target.getAttribute('data-id'));
                    updateRequestStatus(id, 'hold');
                }
            });

            // Filter button handler
            document.getElementById('applyFilters').addEventListener('click', function() {
                renderLeaveRequests();
            });

            // Update request status
            function updateRequestStatus(id, status, reason = '') {
                const request = requests.find(r => r.id === id);
                if (request) {
                    request.status = status;
                    if (reason) request.rejectionReason = reason;
                    renderLeaveRequests();
                }
            }

            // Render leave requests
            function renderLeaveRequests() {
                // Get filter values
                const statusFilter = document.getElementById('filterStatus').value;
                const deptFilter = document.getElementById('filterDepartment').value;
                
                // Filter requests
                let filteredRequests = [...requests];
                if (statusFilter !== 'all') {
                    filteredRequests = filteredRequests.filter(r => r.status === statusFilter);
                }
                if (deptFilter !== 'all') {
                    filteredRequests = filteredRequests.filter(r => r.department === deptFilter);
                }
                
                // Generate HTML
                let html = '';
                filteredRequests.forEach(request => {
                    const startDate = new Date(request.startDate).toLocaleDateString('en-US', { 
                        month: 'short', day: 'numeric', year: 'numeric' 
                    });
                    const endDate = new Date(request.endDate).toLocaleDateString('en-US', { 
                        month: 'short', day: 'numeric', year: 'numeric' 
                    });
                    const dateRange = startDate === endDate ? startDate : `${startDate} - ${endDate}`;
                    
                    const typeMap = {
                        'sick': 'Sick Leave',
                        'casual': 'Casual Leave',
                        'religious': 'Religious Holiday',
                        'national': 'National Holiday'
                    };
                    
                    const statusClass = {
                        'pending': 'status-pending',
                        'approved': 'status-approved',
                        'rejected': 'status-rejected',
                        'hold': 'status-hold'
                    };
                    
                    html += `
                        <div class="leave-card ${statusClass[request.status]} bg-white p-4 rounded-lg shadow-sm border-l-4">
                            <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4">
                                <div>
                                    <h3 class="font-medium text-gray-800">${request.name} (ID: ${request.empId})</h3>
                                    <p class="text-sm text-gray-500">${request.department} Department • ${request.designation}</p>
                                    <div class="mt-2 flex flex-wrap gap-4">
                                        <span class="text-sm"><span class="font-medium">Type:</span> ${typeMap[request.type]}</span>
                                        <span class="text-sm"><span class="font-medium">Dates:</span> ${dateRange}</span>
                                        ${request.reason ? `<span class="text-sm"><span class="font-medium">Reason:</span> ${request.reason}</span>` : ''}
                                        ${request.rejectionReason ? `<span class="text-sm"><span class="font-medium">Remarks:</span> ${request.rejectionReason}</span>` : ''}
                                    </div>
                                </div>
                                ${request.status === 'pending' ? `
                                    <div class="flex space-x-2">
                                        <button class="approve-btn px-3 py-1 bg-green-500 text-white text-xs rounded hover:bg-green-600" data-id="${request.id}">
                                            Approve
                                        </button>
                                        <button class="reject-btn px-3 py-1 bg-red-500 text-white text-xs rounded hover:bg-red-600" data-id="${request.id}">
                                            Reject
                                        </button>
                                        <button class="hold-btn px-3 py-1 bg-blue-500 text-white text-xs rounded hover:bg-blue-600" data-id="${request.id}">
                                            Hold
                                        </button>
                                    </div>
                                ` : `
                                    <div class="text-${request.status === 'approved' ? 'green' : request.status === 'rejected' ? 'red' : 'blue'}-600 font-medium text-sm">
                                        ${request.status.charAt(0).toUpperCase() + request.status.slice(1)}
                                        ${request.rejectionReason ? ` (${request.rejectionReason})` : ''}
                                    </div>
                                `}
                            </div>
                        </div>
                    `;
                });
                
                leaveRequests.innerHTML = html || '<p class="text-gray-500">No leave requests found matching the filters.</p>';
            }
            
            // Initial render
            renderLeaveRequests();
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="New Hire.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TalentOnboard | New Employee Hiring Portal</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        :root {
            --primary: #3b82f6;
            --secondary: #1e40af;
            --accent: #10b981;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc;
            color: #1e293b;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
        }
        
        .benefit-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .form-control:focus {
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.25);
        }
        
        .animate-pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        /* Custom checkbox style */
        .custom-checkbox:checked {
            background-color: var(--primary);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="gradient-bg text-white">
        <div class="container mx-auto px-6 py-12">
            <div class="flex justify-between items-center">
                <div>
                    <h1 class="text-3xl font-bold">Talent<span class="text-blue-200">Onboard</span></h1>
                    <p class="mt-2 text-blue-100">Your journey begins here</p>
                </div>
                <div class="hidden md:block">
                    <img src="https://placehold.co/300x200/1e40af/ffffff?text=Join+Our+Team" alt="Diverse team of professionals collaborating in a modern office space" class="rounded-lg shadow-xl" />
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto px-6 py-12">
        <!-- Hero Section -->
        <section class="mb-16">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div>
                    <h2 class="text-4xl font-bold mb-4">Welcome to Our Growing Team</h2>
                    <p class="text-lg text-gray-600 mb-6">We're excited you're considering joining our organization. At TalentOnboard, we believe in creating an environment where innovation thrives and careers flourish.</p>
                    <div class="flex space-x-4">
                        <button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-medium transition duration-300">Apply Now</button>
                        <button class="border border-blue-600 text-blue-600 px-6 py-3 rounded-lg font-medium transition duration-300 hover:bg-blue-50">Learn More</button>
                    </div>
                </div>
                <div class="hidden lg:block animate-pulse">
                    <img src="https://placehold.co/600x400/3b82f6/ffffff?text=We're+Hiring" alt="Group of diverse professionals celebrating a successful project completion with raised hands" class="rounded-lg shadow-lg" />
                </div>
            </div>
        </section>

        <!-- Hiring Form Section -->
        <section class="mb-16 bg-white rounded-xl shadow-lg overflow-hidden">
            <div class="grid grid-cols-1 lg:grid-cols-2">
                <div class="p-10">
                    <h2 class="text-3xl font-bold mb-6 text-gray-800">Apply Now</h2>
                    <form id="hireForm" class="space-y-6">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="firstName" class="block text-gray-700 font-medium mb-2">First Name</label>
                                <input type="text" id="firstName" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 form-control" required>
                            </div>
                            <div>
                                <label for="lastName" class="block text-gray-700 font-medium mb-2">Last Name</label>
                                <input type="text" id="lastName" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 form-control" required>
                            </div>
                        </div>
                        
                        <div>
                            <label for="email" class="block text-gray-700 font-medium mb-2">Email</label>
                            <input type="email" id="email" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 form-control" required>
                        </div>
                        
                        <div>
                            <label for="phone" class="block text-gray-700 font-medium mb-2">Phone Number</label>
                            <input type="tel" id="phone" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 form-control" required>
                        </div>
                        
                        <div>
                            <label for="position" class="block text-gray-700 font-medium mb-2">Position Applying For</label>
                            <select id="position" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 form-control" required>
                                <option value="" disabled selected>Select a position</option>
                                <option value="developer">Software Developer</option>
                                <option value="designer">UI/UX Designer</option>
                                <option value="marketing">Marketing Specialist</option>
                                <option value="sales">Sales Representative</option>
                                <option value="manager">Project Manager</option>
                            </select>
                        </div>
                        
                        <div>
                            <label for="resume" class="block text-gray-700 font-medium mb-2">Upload Resume</label>
                            <div class="flex items-center justify-center w-full">
                                <label class="flex flex-col w-full h-32 border-2 border-dashed border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50 transition duration-300">
                                    <div class="flex flex-col items-center justify-center pt-7">
                                        <svg class="w(M62)-10 h-10 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"></path>
                                        </svg>
                                        <p class="pt-1 text-sm text-gray-600">Drag and drop your file here or click to browse</p>
                                    </div>
                                    <input type="file" id="resume" class="opacity-0" accept=".pdf,.doc,.docx">
                                </label>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="flex items-center h-5">
                                <input id="terms" aria-describedby="terms" type="checkbox" class="w-4 h-4 border border-gray-300 rounded bg-gray-50 focus:ring-3 focus:ring-blue-300 custom-checkbox" required>
                            </div>
                            <div class="ml-3 text-sm">
                                <label for="terms" class="font-medium text-gray-700">I agree to the <a href="#" class="text-blue-600 hover:underline">terms and conditions</a></label>
                            </div>
                        </div>
                        
                        <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white py-3 px-4 rounded-lg font-medium transition duration-300">Submit Application</button>
                    </form>
                </div>
                
                <div class="hidden lg:block bg-gradient-to-br from-blue-50 to-indigo-50 p-10 flex flex-col justify-center">
                    <div class="text-center">
                        <img src="https://placehold.co/400x300/e0e7ff/3b82f6?text=Career+Opportunities" alt="Modern recruitment process showing handshake between candidate and recruiter in professional setting" class="mx-auto mb-8 rounded-lg" />
                        <h3 class="text-2xl font-bold text-gray-800 mb-4">Why Join Our Team?</h3>
                        <p class="text-gray-600 mb-6">We're looking for talented individuals who are passionate about making a difference. Our hiring process is designed to be transparent, fair, and efficient.</p>
                        <div class="flex justify-center space-x-4">
                            <div class="text-center">
                                <div class="text-3xl font-bold text-blue-600">24h</div>
                                <div class="text-gray-500">Average Response Time</div>
                            </div>
                            <div class="text-center">
                                <div class="text-3xl font-bold text-blue-600">95%</div>
                                <div class="text-gray-500">Candidate Satisfaction</div>
                            </div>
                            <div class="text-center">
                                <div class="text-3xl font-bold text-blue-600">3</div>
                                <div class="text-gray-500">Interview Stages</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Benefits Section -->
        <section class="mb-16">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Employee Benefits</h2>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">We invest in our team's well-being and professional growth with comprehensive benefits packages.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <div class="bg-white rounded-xl shadow-md p-6 transition duration-300 benefit-card">
                    <div class="flex justify-center mb-4">
                        <div class="bg-blue-100 p-4 rounded-full">
                            <svg class="w-8 h-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                            </svg>
                        </div>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 text-gray-800">Career Growth</h3>
                    <p class="text-gray-600 text-center">Continuous learning opportunities and clear paths for advancement within the company.</p>
                </div>
                
                <div class="bg-white rounded-xl shadow-md p-6 transition duration-300 benefit-card">
                    <div class="flex justify-center mb-4">
                        <div class="bg-green-100 p-4 rounded-full">
                            <svg class="w-8 h-8 text-green-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 9V7a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2m2 4h10a2 2 0 002-2v-6a2 2 0 00-2-2H9a2 2 0 00-2 2v6a2 2 0 002 2zm7-5a2 2 0 11-4 0 2 2 0 014 0z"></path>
                            </svg>
                        </div>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 text-gray-800">Competitive Pay</h3>
                    <p class="text-gray-600 text-center">Industry-leading compensation packages with performance bonuses and regular reviews.</p>
                </div>
                
                <div class="bg-white rounded-xl shadow-md p-6 transition duration-300 benefit-card">
                    <div class="flex justify-center mb-4">
                        <div class="bg-purple-100 p-4 rounded-full">
                            <svg class="w-8 h-8 text-purple-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 116 0v6a3 3 0 01-3 3z"></path>
                            </svg>
                        </div>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 text-gray-800">Flexible Work</h3>
                    <p class="text-gray-600 text-center">Hybrid work options with flexible schedules to support work-life balance.</p>
                </div>
                
                <div class="bg-white rounded-xl shadow-md p-6 transition duration-300 benefit-card">
                    <div class="flex justify-center mb-4">
                        <div class="bg-yellow-100 p-4 rounded-full">
                            <svg class="w-8 h-8 text-yellow-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                            </svg>
                        </div>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 text-gray-800">Generous PTO</h3>
                    <p class="text-gray-600 text-center">Ample vacation days plus holidays and paid time off for volunteering.</p>
                </div>
            </div>
        </section>

        <!-- Hiring Process Section -->
        <section class="mb-16">
            <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-2">
                    <div class="p-10">
                        <h2 class="text-3xl font-bold mb-6 text-gray-800">Our Hiring Process</h2>
                        <p class="text-gray-600 mb-8">We've designed our hiring process to be thorough yet efficient, ensuring we make the best matches between candidates and roles.</p>
                        
                        <div class="space-y-8">
                            <div class="flex">
                                <div class="flex-shrink-0 mr-4">
                                    <div class="flex items-center justify-center h-12 w-12 rounded-full bg-blue-100 text-blue-600 font-bold">1</div>
                                </div>
                                <div>
                                    <h4 class="text-lg font-semibold text-gray-800">Initial Application</h4>
                                    <p class="text-gray-600">Submit your details through our secure portal. Make sure to include an updated resume.</p>
                                </div>
                            </div>
                            
                            <div class="flex">
                                <div class="flex-shrink-0 mr-4">
                                    <div class="flex items-center justify-center h-12 w-12 rounded-full bg-blue-100 text-blue-600 font-bold">2</div>
                                </div>
                                <div>
                                    <h4 class="text-lg font-semibold text-gray-800">Screening Call</h4>
                                    <p class="text-gray-600">A 30-minute phone conversation to discuss your experience and answer initial questions.</p>
                                </div>
                            </div>
                            
                            <div class="flex">
                                <div class="flex-shrink-0 mr-4">
                                    <div class="flex items-center justify-center h-12 w-12 rounded-full bg-blue-100 text-blue-600 font-bold">3</div>
                                </div>
                                <div>
                                    <h4 class="text-lg font-semibold text-gray-800">Technical/Skills Assessment</h4>
                                    <p class="text-gray-600">Role-specific evaluation to demonstrate your capabilities in a realistic scenario.</p>
                                </div>
                            </div>
                            
                            <div class="flex">
                                <div class="flex-shrink-0 mr-4">
                                    <div class="flex items-center justify-center h-12 w-12 rounded-full bg-blue-100 text-blue-600 font-bold">4</div>
                                </div>
                                <div>
                                    <h4 class="text-lg font-semibold text-gray-800">Final Interviews</h4>
                                    <p class="text-gray-600">Meetings with potential future colleagues and leadership to ensure mutual fit.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="hidden lg:block bg-gray-50 p-10 flex items-center">
                        <img src="https://placehold.co/500x350/f8fafc/3b82f6?text=Transparent+Hiring+Process" alt="Infographic showing the four-step hiring process with progress indicators and timeline" class="rounded-lg shadow-md w-full" />
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="container mx-auto px-6">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-xl font-bold mb-4">TalentOnboard</h3>
                    <p class="text-gray-400">Building exceptional teams through thoughtful hiring.</p>
                </div>
                
                <div>
                    <h4 class="font-semibold text-gray-300 mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Current Openings</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Employee Stories</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Diversity & Inclusion</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Hiring Process</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="font-semibold text-gray-300 mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Candidate FAQ</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Interview Tips</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Resume Guide</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Employee Benefits</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="font-semibold text-gray-300 mb-4">Contact Us</h4>
                    <address class="not-italic text-gray-400">
                        <p class="mb-2">123 Talent Avenue</p>
                        <p class="mb-2">San Francisco, CA 94102</p>
                        <p class="mb-2">Email: careers@talentonboard.com</p>
                        <p>Phone: (555) 123-4567</p>
                    </address>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
                <p>© 2023 TalentOnboard. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Form Submission Modal -->
    <div id="successModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
        <div class="bg-white rounded-lg shadow-xl p-8 max-w-md w-full mx-4">
            <div class="flex justify-center mb-6">
                <div class="bg-green-100 p-4 rounded-full">
                    <svg class="w-12 h-12 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                </div>
            </div>
            <h3 class="text-2xl font-bold text-center mb-4 text-gray-800">Application Submitted!</h3>
            <p class="text-gray-600 text-center mb-6">Thank you for applying to join our team. We've received your application and will review it shortly.</p>
            <button id="closeModal" class="w-full bg-blue-600 hover:bg-blue-700 text-white py-3 px-4 rounded-lg font-medium transition duration-300">Close</button>
        </div>
    </div>

    <script>
        // Form submission handling
        document.getElementById('hireForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Simulate form submission
            setTimeout(() => {
                document.getElementById('successModal').classList.remove('hidden');
            }, 1000);
        });
        
        // Close modal handling
        document.getElementById('closeModal').addEventListener('click', function() {
            document.getElementById('successModal').classList.add('hidden');
            document.getElementById('hireForm').reset();
        });
        
        // File upload styling enhancement
        const fileInput = document.getElementById('resume');
        const fileUploadDiv = fileInput.parentElement.parentElement;
        
        fileInput.addEventListener('change', function() {
            if (fileInput.files.length > 0) {
                fileUploadDiv.classList.add('border-blue-500');
                fileUploadDiv.classList.remove('border-gray-300');
                fileUploadDiv.querySelector('p').textContent = fileInput.files[0].name;
            } else {
                fileUploadDiv.classList.remove('border-blue-500');
                fileUploadDiv.classList.add('border-gray-300');
                fileUploadDiv.querySelector('p').textContent = 'Drag and drop your file here or click to browse';
            }
        });
        
        // Position select validation
        document.getElementById('position').addEventListener('change', function() {
            if (this.value !== '') {
                this.classList.remove('border-gray-300');
                this.classList.add('border-blue-500');
            } else {
                this.classList.remove('border-blue-500');
                this.classList.add('border-gray-300');
            }
        });
    </script>
</body>
</html>
```

This comprehensive hiring page includes:
1. A modern, responsive design using Tailwind CSS
2. Complete application form with validation
3. Company introduction section
4. Employee benefits display with icons
5. Detailed hiring process explanation
6. Professional footer with contact information
7. Form submission modal
8. Interactive JavaScript elements for better UX
9. Optimized for both desktop and mobile viewing
10. Carefully selected images with descriptive alt text for automatic generation

The page has been designed to make the hiring process clear and inviting for potential candidates while collecting all necessary application information.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Offer Letter Generator | Lavanya Healthcare</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- Tailwind CDN for styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- html2pdf JS library for PDF download -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    <style>
        /* Watermark for Lavanya Healthcare */
        .watermark {
            position: absolute;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-20deg);
            opacity: 0.08;
            font-size: 5rem;
            font-weight: 900;
            color: #3182ce;
            pointer-events: none;
            user-select: none;
            z-index: 0;
        }
        @media print {
            .no-print { display: none; }
            body { background: #fff !important; }
            #letter-card { box-shadow: none !important; }
        }
    </style>
</head>
<body class="bg-blue-50 min-h-screen flex flex-col items-center py-8">

    <!-- Card Container -->
    <div class="bg-white shadow-2xl rounded-xl p-8 w-full max-w-3xl relative" id="letter-card">
        <!-- Watermark -->
        <span class="watermark select-none">Lavanya Healthcare</span>
        <!-- Logo & Title -->
        <div class="flex flex-col items-center mb-8 relative z-10">
            <img src="logo.jpg"mb-3">
            <h1 class="text-2xl font-bold tracking-wide text-blue-800">Lavanya Healthcare Limited</h1>
            <p class="text-gray-700 text-sm mt-1">Registered Office: Lavanya Healthcare Ltd.
Khewat No. 359/310, Behra Road,
Dera Bassi, Mohali - 140507</p>
            <p class="text-gray-600 text-xs">hr@lavanyahealthcare.com | +91 9050345121</p>
        </div>

        <!-- Step 1: User Form -->
        <form id="empForm" class="no-print relative z-10 space-y-4 mb-8">
            <div class="grid md:grid-cols-2 gap-5">
                <div>
                    <label class="block text-gray-700 font-medium mb-1">Employee Name</label>
                    <input type="text" id="empName" class="w-full border rounded px-2 py-2" placeholder="e.g. Lavanya Healthcare" required>
                </div>
                <div>
                    <label class="block text-gray-700 font-medium mb-1">Department</label>
                    <select id="empDept" class="w-full border rounded px-2 py-2" required>
                        <option value="">Select</option>
                        <option>Nursing</option><option>Doctor</option><option>Administration</option>
                        <option>HR</option><option>Finance</option><option>IT</option>
                        <option>Pharmacy</option><option>Laboratory</option><option>Housekeeping</option>
                    </select>
                </div>
                <div>
                    <label class="block text-gray-700 font-medium mb-1">Designation</label>
                    <input type="text" id="empDesig" class="w-full border rounded px-2 py-2" placeholder="e.g. Junior Accountant" required>
                </div>
                <div>
                    <label class="block text-gray-700 font-medium mb-1">Salary Offer &#40;₹&#41;</label>
                    <input type="number" min="0" id="empSalary" class="w-full border rounded px-2 py-2" placeholder="e.g. 35000" required>
                </div>
                <div>
                    <label class="block text-gray-700 font-medium mb-1">Date of Joining</label>
                    <input type="date" id="empDoj" class="w-full border rounded px-2 py-2" required>
                </div>
                <div>
                    <label class="block text-gray-700 font-medium mb-1">Offer Date</label>
                    <input type="date" id="empOfferDate" class="w-full border rounded px-2 py-2" required>
                </div>
            </div>
            <div class="flex justify-center gap-4 pt-4">
                <button type="submit" class="bg-blue-600 hover:bg-blue-700 text-white rounded px-5 py-2 font-medium">Generate Letter</button>
                <button type="button" id="resetBtn" class="bg-gray-200 hover:bg-gray-300 rounded px-4 py-2 font-medium text-gray-800">Reset</button>
            </div>
        </form>

        <!-- Offer Letter Preview (hidden until generated) -->
        <section id="letterPreview" class="hidden relative z-20">
            <div class="text-sm">
                <div class="flex justify-between mb-3">
                    <span></span>
                    <span>Date: <span id="displayOfferDate"></span></span>
                </div>
                <div class="mb-4">
                    To, <br>
                    <span id="displayEmpName" class="font-semibold"></span><br>
                    <span id="displayEmpDesig"></span><br>
                    <span id="displayEmpDept"></span>
                </div>
                <div class="mb-2 font-semibold">Subject: Offer of Employment</div>
                <div class="mb-2">Dear <span id="displaySalutation"></span>,</div>
                <div class="mb-3">
                    <p>
                    We are pleased to offer you the position of <b><span id="displayEmpDesig2"></span></b> 
                    in the <b><span id="displayEmpDept2"></span></b> department at Lavanya Healthcare Limited,
                    effective from <b><span id="displayEmpDoj"></span></b>.<br><br>
                    The terms and conditions of your employment are as follows:
                    </p>
                    <ol class="pl-7 mt-3 mb-2 space-y-2 list-decimal">
                        <li>
                            You will be paid a gross monthly salary of <b>₹ <span id="displaySalaryNum"></span></b>
                            (<i><span id="displaySalaryWord"></span></i> only), subject to taxes/deductions.
                        </li>
                        <li>Your employment is subject to Lavanya Healthcare’s policies and norms.</li>
                        <li>You will be on probation for 3 months, extendable at management’s discretion.</li>
                        <li>On confirmation, you will be eligible for benefits as per policy.</li>
                        <li>You will report to your Department Head or as assigned.</li>
                    </ol>
                    <p>
                        This offer is conditional on document/background verification.<br>
                        Please confirm acceptance by signing and returning within 7 days.
                    </p>
                </div>
                <div class="mt-5 mb-2">
                    We look forward to welcoming you to our team!
                </div>
                <div class="mt-8">
                    Yours sincerely,<br><br>
                    <b>For Lavanya Healthcare Limited</b><br><br>
                        Authorized Signatory
                    <img src="https://placehold.co/120x32?text=Sign" alt="Authorized Sign" class="mb-1">
                    <br>
                </div>
                <div class="mt-12">
                    _________________<br>
                    <span class="text-xs">Signature of Candidate</span>
                </div>
                <div class="mt-6 text-center text-gray-500 text-xs">
                </div>
            </div>

            <!-- Action Buttons -->
            <div class="flex flex-wrap justify-center gap-4 mt-6 no-print">
                <button onclick="window.print()" class="bg-green-600 hover:bg-green-700 text-white px-6 py-2 rounded font-medium">Print</button>
                <button onclick="dlPDF()" class="bg-purple-700 hover:bg-purple-900 text-white px-6 py-2 rounded font-medium">Download as PDF</button>
                <button onclick="restartForm()" class="bg-gray-400 hover:bg-gray-600 text-white px-5 py-2 rounded font-medium">Back/Edit</button>
            </div>
        </section>
    </div>

<script>
/* --- Utility Functions --- */
// Indian number format (lakh, crore)
function formatINR(n) {
    n = Number(n);
    return n.toLocaleString('en-IN');
}

// Number to words (INR, lakhs/crores covered)
function numToWords(num) {
    if (typeof(num)==='string') num=Number(num);
    if (isNaN(num)) return '';
    if (num===0) return "zero rupees";
    let arr1 = ['', 'one', 'two', 'three', 'four', 'five', 'six', 'seven', 'eight', 'nine', 'ten', 'eleven', 'twelve', 'thirteen', 'fourteen', 'fifteen', 'sixteen', 'seventeen', 'eighteen', 'nineteen'];
    let arr2 = ['', '', 'twenty', 'thirty', 'forty', 'fifty', 'sixty', 'seventy', 'eighty', 'ninety'];
    let str = '';
    function words(n) {
        if (n < 20) return arr1[n];
        if (n < 100) return arr2[Math.floor(n/10)] + (n%10!==0?' ' + arr1[n%10]:'');
        if (n < 1000) return arr1[Math.floor(n/100)] + ' hundred' + ((n%100!==0)?' and '+words(n%100):'');
        if (n < 100000) return words(Math.floor(n/1000)) + ' thousand' + ((n%1000!==0)?' '+words(n%1000):'');
        if (n < 10000000) return words(Math.floor(n/100000)) + ' lakh' + ((n%100000!==0)?' '+words(n%100000):'');
        return words(Math.floor(n/10000000)) + ' crore' + ((n%10000000!==0)?' '+words(n%10000000):'');
    }
    str = words(num);
    return str + ' rupees';
}

// Indian Date Format
function formatDateIndian(isoStr) {
    if (!isoStr) return '';
    let date = new Date(isoStr);
    return date.toLocaleDateString('en-IN', {year:'numeric', month:'long', day:'numeric'});
}

/* -- Letter Generation Handler -- */

const form = document.getElementById('empForm');
form.onsubmit = function(e){
    e.preventDefault();
    // Gather form values
    let name=document.getElementById('empName').value.trim();
    let dept=document.getElementById('empDept').value;
    let desig=document.getElementById('empDesig').value.trim();
    let salary=document.getElementById('empSalary').value.trim();
    let doj=document.getElementById('empDoj').value;
    let offerDate=document.getElementById('empOfferDate').value;
    // Validation
    if(!name || !dept || !desig || !salary || !doj || !offerDate){
        alert('Please fill in all fields!');
        return false;
    }
    // Fill letter
    document.getElementById('displayEmpName').textContent = name;
    document.getElementById('displayEmpDesig').textContent = desig;
    document.getElementById('displayEmpDept').textContent = dept;
    document.getElementById('displayEmpDesig2').textContent = desig;
    document.getElementById('displayEmpDept2').textContent = dept;
    document.getElementById('displaySalaryNum').textContent = formatINR(salary);
    document.getElementById('displaySalaryWord').textContent = numToWords(salary).replace(/\b\w/g, l=>l.toUpperCase());
    document.getElementById('displayEmpDoj').textContent = formatDateIndian(doj);
    document.getElementById('displayOfferDate').textContent = formatDateIndian(offerDate);
    document.getElementById('displaySalutation').textContent = name.split(' ')[0];
    // Show letter, hide form
    form.classList.add('hidden');
    document.getElementById('letterPreview').classList.remove('hidden');
    return false;
};

// Back to edit/reset handler
function restartForm(){
    document.getElementById('letterPreview').classList.add('hidden');
    document.getElementById('empForm').classList.remove('hidden');
}

// PDF Save
function dlPDF(){
    let el = document.getElementById('letterPreview');
    let opt = {
        margin: [15,10],
        filename: 'Offer_Letter_LavanyaHealthcare.pdf',
        html2canvas: {scale: 2},
        image: {type: 'jpeg', quality:0.96},
        jsPDF: {unit: 'mm', format: 'a4', orientation: 'portrait'}
    };
    html2pdf().from(el).set(opt).save();
}

// Reset all
document.getElementById('resetBtn').onclick = function(){
    form.reset();
};

/* --- Pre-fill default Offer Date (today) and DoJ (next Monday) --- */
window.onload = function(){
    let today = new Date();
    // Set offer date to today
    document.getElementById('empOfferDate').value = today.toISOString().slice(0,10);
    // Set DoJ to next Monday
    let nextMonday = new Date(today);
    nextMonday.setDate(today.getDate() + ((8 - today.getDay()) % 7 || 7));
    document.getElementById('empDoj').value = nextMonday.toISOString().slice(0,10);
};
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Indian Salary Slip Generator</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f5f7fa;
        }
        
        .salary-slip {
            border: 1px solid #e2e8f0;
            background-color: white;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }
        
        .header-bg {
            background-color: #2563eb;
        }
        
        .divider {
            border-bottom: 1px solid #e2e8f0;
        }
        
        .rupee-symbol {
            font-family: Arial, sans-serif;
        }
        
        @media print {
            .no-print {
                display: none !important;
            }
            body, .salary-slip {
                background-color: white;
                box-shadow: none;
            }
        }
    </style>
</head>
<body class="min-h-screen py-8 px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto">
        <h1 class="text-3xl font-bold text-center text-gray-800 mb-8">Indian Salary Slip Generator</h1>
        
        <!-- Salary Input Form -->
        <div class="no-print bg-white rounded-lg shadow-md p-6 mb-8">
            <h2 class="text-xl font-semibold text-gray-700 mb-4">Salary Details</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <!-- Employee Details -->
                <div class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Employee Name</label>
                        <input type="text" id="employeeName" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Employee ID</label>
                        <input type="text" id="employeeId" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Month & Year</label>
                        <input type="month" id="salaryMonth" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                    </div>
                </div>
                
                <!-- Earnings -->
                <div class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Basic Salary (₹)</label>
                        <input type="number" id="basicSalary" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500" min="0" value="0">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">HRA (₹)</label>
                        <input type="number" id="hra" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500" min="0" value="0">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Special Allowance (₹)</label>
                        <input type="number" id="specialAllowance" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500" min="0" value="0">
                    </div>
                </div>
            </div>
            
            <!-- Deductions -->
            <div class="mt-6">
                <h3 class="text-md font-semibold text-gray-700 mb-2">Deductions</h3>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Provident Fund (₹)</label>
                        <input type="number" id="pf" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500" min="0" value="0">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Professional Tax (₹)</label>
                        <input type="number" id="professionalTax" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500" min="0" value="0">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">TDS (₹)</label>
                        <input type="number" id="tds" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500" min="0" value="0">
                    </div>
                </div>
            </div>
            
            <div class="mt-6 flex justify-center">
                <button onclick="generateSalarySlip()" class="px-4 py-2 bg-blue-600 text-white rounded-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
                    Generate Salary Slip
                </button>
            </div>
        </div>
        
        <!-- Salary Slip Preview -->
        <div id="salarySlipContainer" class="salary-slip rounded-lg overflow-hidden hidden">
            <div class="header-bg py-4 px-6">
                <div class="flex justify-between items-center">
                    <div>
                        <h2 id="companyName" class="text-2xl font-bold text-white">Company Name Pvt. Ltd.</h2>
                        <p class="text-blue-100">Salary Slip</p>
                    </div>
                    <img src="https://placehold.co/100x100" alt="Company logo with dark blue background and white text" class="h-16 w-16 bg-white p-2 rounded-full" />
                </div>
            </div>
            
            <div class="p-6">
                <!-- Employee Info -->
                <div class="flex flex-col md:flex-row justify-between mb-6">
                    <div>
                        <p class="text-sm text-gray-500">Employee Name</p>
                        <p id="slipEmployeeName" class="font-medium">-</p>
                    </div>
                    <div>
                        <p class="text-sm text-gray-500">Employee ID</p>
                        <p id="slipEmployeeId" class="font-medium">-</p>
                    </div>
                    <div>
                        <p class="text-sm text-gray-500">Month & Year</p>
                        <p id="slipSalaryMonth" class="font-medium">-</p>
                    </div>
                </div>
                
                <!-- Salary Details -->
                <h3 class="text-lg font-semibold text-gray-800 mb-2">Earnings</h3>
                <div class="divide-y divide-gray-200">
                    <div class="py-2 flex justify-between">
                        <span>Basic Salary</span>
                        <span id="slipBasicSalary" class="rupee-symbol font-medium">₹0</span>
                    </div>
                    <div class="py-2 flex justify-between">
                        <span>House Rent Allowance (HRA)</span>
                        <span id="slipHra" class="rupee-symbol font-medium">₹0</span>
                    </div>
                    <div class="py-2 flex justify-between">
                        <span>Special Allowance</span>
                        <span id="slipSpecialAllowance" class="rupee-symbol font-medium">₹0</span>
                    </div>
                </div>
                
                <div class="mt-4">
                    <div class="py-2 flex justify-between bg-blue-50 px-2 rounded">
                        <span class="font-semibold">Gross Salary</span>
                        <span id="slipGrossSalary" class="rupee-symbol font-bold">₹0</span>
                    </div>
                </div>
                
                <h3 class="text-lg font-semibold text-gray-800 mt-6 mb-2">Deductions</h3>
                <div class="divide-y divide-gray-200">
                    <div class="py-2 flex justify-between">
                        <span>Provident Fund (PF)</span>
                        <span id="slipPf" class="rupee-symbol font-medium">₹0</span>
                    </div>
                    <div class="py-2 flex justify-between">
                        <span>Professional Tax</span>
                        <span id="slipProfessionalTax" class="rupee-symbol font-medium">₹0</span>
                    </div>
                    <div class="py-2 flex justify-between">
                        <span>Tax Deducted at Source (TDS)</span>
                        <span id="slipTds" class="rupee-symbol font-medium">₹0</span>
                    </div>
                </div>
                
                <div class="mt-4">
                    <div class="py-2 flex justify-between bg-blue-50 px-2 rounded">
                        <span class="font-semibold">Total Deductions</span>
                        <span id="slipTotalDeductions" class="rupee-symbol font-bold">₹0</span>
                    </div>
                </div>
                
                <!-- Net Salary -->
                <div class="mt-6 py-3 px-4 bg-green-50 rounded border border-green-100">
                    <div class="flex justify-between items-center">
                        <span class="font-bold text-lg">Net Salary Payable</span>
                        <span id="slipNetSalary" class="rupee-symbol text-2xl font-bold text-green-700">₹0</span>
                    </div>
                </div>
                
                <!-- Footer -->
                <div class="mt-8 pt-4 divider">
                    <div class="flex justify-between text-sm text-gray-500">
                        <div>
                            <p>Generated on: <span id="generationDate">-</span></p>
                        </div>
                        <div class="text-right">
                            <p>For any queries, contact HR</p>
                            <p>Email: hr@company.com</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="px-6 py-4 bg-gray-50 flex justify-center no-print">
                <button onclick="window.print()" class="px-4 py-2 bg-blue-600 text-white rounded-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 mr-3">
                    Print Salary Slip
                </button>
                <button onclick="downloadAsPDF()" class="px-4 py-2 bg-green-600 text-white rounded-md hover:bg-green-700 focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-offset-2">
                    Download as PDF
                </button>
            </div>
        </div>
    </div>

    <script>
        // Format Indian Rupees
        function formatINR(amount) {
            return '₹' + Number(amount).toLocaleString('en-IN');
        }
        
        // Calculate salary components
        function generateSalarySlip() {
            // Get input values
            const employeeName = document.getElementById('employeeName').value || 'Not Provided';
            const employeeId = document.getElementById('employeeId').value || 'N/A';
            const salaryMonth = document.getElementById('salaryMonth').value || 'Not Selected';
            
            const basicSalary = parseFloat(document.getElementById('basicSalary').value) || 0;
            const hra = parseFloat(document.getElementById('hra').value) || 0;
            const specialAllowance = parseFloat(document.getElementById('specialAllowance').value) || 0;
            
            const pf = parseFloat(document.getElementById('pf').value) || 0;
            const professionalTax = parseFloat(document.getElementById('professionalTax').value) || 0;
            const tds = parseFloat(document.getElementById('tds').value) || 0;
            
            // Calculate totals
            const grossSalary = basicSalary + hra + specialAllowance;
            const totalDeductions = pf + professionalTax + tds;
            const netSalary = grossSalary - totalDeductions;
            
            // Update the salary slip
            document.getElementById('slipEmployeeName').textContent = employeeName;
            document.getElementById('slipEmployeeId').textContent = employeeId;
            
            // Format month and year (from YYYY-MM to Month, YYYY)
            if (salaryMonth !== 'Not Selected') {
                const [year, month] = salaryMonth.split('-');
                const monthNames = ["January", "February", "March", "April", "May", "June",
                                    "July", "August", "September", "October", "November", "December"];
                document.getElementById('slipSalaryMonth').textContent = `${monthNames[parseInt(month) - 1]}, ${year}`;
            } else {
                document.getElementById('slipSalaryMonth').textContent = 'Not Selected';
            }
            
            document.getElementById('slipBasicSalary').textContent = formatINR(basicSalary);
            document.getElementById('slipHra').textContent = formatINR(hra);
            document.getElementById('slipSpecialAllowance').textContent = formatINR(specialAllowance);
            document.getElementById('slipGrossSalary').textContent = formatINR(grossSalary);
            
            document.getElementById('slipPf').textContent = formatINR(pf);
            document.getElementById('slipProfessionalTax').textContent = formatINR(professionalTax);
            document.getElementById('slipTds').textContent = formatINR(tds);
            document.getElementById('slipTotalDeductions').textContent = formatINR(totalDeductions);
            
            document.getElementById('slipNetSalary').textContent = formatINR(netSalary);
            
            // Set current date
            const today = new Date();
            document.getElementById('generationDate').textContent = today.toLocaleDateString('en-IN', {
                day: 'numeric',
                month: 'short',
                year: 'numeric'
            });
            
            // Show the salary slip
            document.getElementById('salarySlipContainer').classList.remove('hidden');
            
            // Scroll to the salary slip
            document.getElementById('salarySlipContainer').scrollIntoView({
                behavior: 'smooth'
            });
        }
        
        // PDF download functionality (placeholder - would need a library like jsPDF in a real implementation)
        function downloadAsPDF() {
            alert('In a real implementation, this would download the salary slip as a PDF using a library like jsPDF.');
        }
        
        // Auto-calculate HRA as 40% of basic salary when basic changes
        document.getElementById('basicSalary').addEventListener('input', function() {
            const basic = parseFloat(this.value) || 0;
            document.getElementById('hra').value = Math.round(basic * 0.4);
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Salary Sheet</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        table {
            border-collapse: separate;
            border-spacing: 0;
        }
        th, td {
            border-bottom: 1px solid #e5e7eb;
        }
        tr:hover {
            background-color: #f9fafb;
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded hover:bg-blue-500">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded active">Salary</a></li>
                        <li><a href="Attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attendance</a></li>
                        <li><a href="Attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hires</a></li>
                    </ul>
                </nav>
            </div>
        </header>

        <!-- Main Content -->
        <main class="flex-grow container mx-auto px-4 py-8">
            <div class="flex justify-between items-center mb-8">
                <h2 class="text-2xl font-bold text-gray-800">Salary Management</h2>
                <div class="flex space-x-4">
                    <button class="bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 rounded-lg flex items-center">
                        <img src="https://placehold.co/20x20" alt="Dollar icon representing salary processing" class="mr-2"> Process Payroll
                    </button>
                    <button class="border border-blue-600 text-blue-600 hover:bg-blue-50 px-4 py-2 rounded-lg flex items-center">
                        <img src="https://placehold.co/20x20" alt="Download icon for exporting salary data" class="mr-2"> Export
                    </button>
                </div>
            </div>

            <div class="bg-white rounded-lg shadow-md overflow-hidden mb-6">
                <div class="p-4 border-b">
                    <div class="flex flex-wrap justify-between items-center">
                        <div class="mb-4 md:mb-0">
                            <label class="block text-gray-700 mb-1">Month</label>
                            <select class="border rounded-lg px-3 py-2">
                                <option>January 2025</option>
                                <option>February 2025</option>
                                <option>March 2025</option>
                                <option>April 2025</option>
                                       <option>May 2025</option>
                                        <option>June 2025</option>
                                 <option>July 2025</option>
                              <option>August 2025</option>
                            <option>September 2025</option>
                            <option>October 2025</option>
                                  <option>November 2025</option>
                           <option>December 2025</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-gray-700 mb-1">Search</label>
                            <input type="text" placeholder="Search employees..." class="border rounded-lg px-3 py-2 w-full md:w-64">
                        </div>
                    </div>
                </div>
                
                <div class="overflow-x-auto">
                    <table class="w-full">
                        <thead class="bg-gray-50">
                            <tr class="text-left text-gray-500">
                                <th class="px-6 py-3">Employee ID</th>
                                <th class="px-6 py-3">Name</th>
                                <th class="px-6 py-3">Basic Salary</th>
                                <th class="px-6 py-3">Allowances</th>
                                <th class="px-6 py-3">Deductions</th>
                                <th class="px-6 py-3">Net Pay</th>
                                <th class="px-6 py-3">Status</th>
                                <th class="px-6 py-3">Actions</th>
                            </tr>
                        </thead>
                        <tbody class="text-gray-700">
                            <tr>
                                <td class="px-6 py-4">EMP001</td>
                                <td class="px-6 py-4">John Doe</td>
                                <td class="px-6 py-4">$5,000.00</td>
                                <td class="px-6 py-4">$800.00</td>
                                <td class="px-6 py-4">$450.00</td>
                                <td class="px-6 py-4 font-semibold">$5,350.00</td>
                                <td class="px-6 py-4"><span class="bg-green-100 text-green-800 px-2 py-1 rounded-full text-xs">Paid</span></td>
                                <td class="px-6 py-4">
                                    <button class="text-blue-600 hover:text-blue-800 mr-2"><li><a href="salary slip.html" class="px-3 py-2 rounded hover:bg-blue-500">Generate Salary Slip</a></li></button></button></button>
                                    <button class="text-gray-600 hover:text-gray-800">
                                </td>
                            </tr>
                            <tr>
                                <td class="px-6 py-4">EMP002</td>
                                <td class="px-6 py-4">vikram</td>
                                <td class="px-6 py-4">₹20000.00</td>
                                <td class="px-6 py-4">₹2500</td>
                                <td class="px-6 py-4">₹17500</td>
                                <td class="px-6 py-4 font-semibold">₹17500</td>
                                <td class="px-6 py-4"><span class="bg-green-100 text-green-800 px-2 py-1 rounded-full text-xs">Paid</span></td>
                                <td class="px-6 py-4">
                                    <button class="text-blue-600 hover:text-blue-800 mr-2"><li><a href="salary slip.html" class="px-3 py-2 rounded hover:bg-blue-500">Generate Salary Slip</a></li></button>
                                    <button class="text-gray-600 hover:text-gray-800">
                                </td>
                            </tr>
                            <tr>
                                <td class="px-6 py-4">EMP003</td>
                                <td class="px-6 py-4">Robert Johnson</td>
                                <td class="px-6 py-4">$4,200.00</td>
                                <td class="px-6 py-4">$600.00</td>
                                <td class="px-6 py-4">$380.00</td>
                                <td class="px-6 py-4 font-semibold">$4,420.00</td>
                                <td class="px-6 py-4"><span class="bg-yellow-100 text-yellow-800 px-2 py-1 rounded-full text-xs">Pending</span></td>
                                <td class="px-6 py-4">
                                    <button class="text-blue-600 hover:text-blue-800 mr-2"><li><a href="salary slip.html" class="px-3 py-2 rounded hover:bg-blue-500">Generate Salary Slip</a></li></button></button>
                                    <button class="text-gray-600 hover:text-gray-800"></button>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <div class="p-4 border-t flex justify-between items-center">
                    <div class="text-gray-500">
                        Showing 1 to 3 of 15 entries
                    </div>
                    <div class="flex space-x-2">
                        <button class="px-3 py-1 border rounded-md">Previous</button>
                        <button class="px-3 py-1 border rounded-md bg-blue-600 text-white">1</button>
                        <button class="px-3 py-1 border rounded-md">2</button>
                        <button class="px-3 py-1 border rounded-md">3</button>
                        <button class="px-3 py-1 border rounded-md">Next</button>
                    </div>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
                <div class="bg-white rounded-lg shadow-md p-6">
                    <div class="flex justify-between items-center mb-4">
                        <h3 class="text-lg font-semibold text-gray-800">Salary Summary</h3>
                        <span class="bg-blue-100 text-blue-800 px-2 py-1 rounded-full text-xs">Current Month</span>
                    </div>
                    <div class="space-y-4">
                        <div class="flex justify-between">
                            <span class="text-gray-600">Total Basic</span>
                            <span class="font-semibold">$15,700.00</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-gray-600">Total Allowances</span>
                            <span class="font-semibold">$2,600.00</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-gray-600">Total Deductions</span>
                            <span class="font-semibold">$1,350.00</span>
                        </div>
                        <div class="pt-4 border-t">
                            <div class="flex justify-between">
                                <span class="text-gray-800 font-bold">Net Payroll</span>
                                <span class="text-blue-600 font-bold">$16,950.00</span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-lg font-semibold text-gray-800 mb-4">Salary Distribution</h3>
                    <div class="flex justify-center mb-4">
                        <img src="https://placehold.co/200x200" alt="Pie chart showing salary distribution by department with color-coded segments" class="w-40 h-40">
                    </div>
                    <div class="space-y-2">
                        <div class="flex items-center">
                            <span class="w-3 h-3 bg-blue-500 rounded-full mr-2"></span>
                            <span class="text-gray-600 text-sm">IT Department (45%)</span>
                        </div>
                        <div class="flex items-center">
                            <span class="w-3 h-3 bg-green-500 rounded-full mr-2"></span>
                            <span class="text-gray-600 text-sm">HR (20%)</span>
                        </div>
                        <div class="flex items-center">
                            <span class="w-3 h-3 bg-yellow-500 rounded-full mr-2"></span>
                            <span class="text-gray-600 text-sm">Finance (25%)</span>
                        </div>
                        <div class="flex items-center">
                            <span class="w-3 h-3 bg-red-500 rounded-full mr-2"></span>
                            <span class="text-gray-600 text-sm">Operations (10%)</span>
                        </div>
                    </div>
                </div>

                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-lg font-semibold text-gray-800 mb-4">Salary Trends</h3>
                    <div class="flex justify-center mb-4">
                        <img src="https://placehold.co/200x100" alt="Line chart showing monthly salary trends over the last year with upward trend line" class="w-full h-32">
                    </div>
                    <div class="text-center text-gray-600 text-sm">
                        Monthly payroll trend for the past 12 months
                    </div>
                </div>
            </div>
        </main>

        <!-- Footer -->
        <footer class="bg-gray-800 text-white py-8">
            <div class="container mx-auto px-4">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <div class="mb-4 md:mb-0">
                        <h3 class="text-xl font-bold mb-2">HR Dashboard</h3>
                        <p class="text-gray-400">© 2025 Company Name. All rights reserved.</p>
                    </div>
                    <nav>
                        <ul class="flex space-x-6">
                            <li><a href="index.html" class="hover:text-blue-400">Home</a></li>
                            <li><a href="privacy.html" class="hover:text-blue-400">Privacy Policy</a></li>
                            <li><a href="terms.html" class="hover:text-blue-400">Terms</a></li>
                            <li><a href="contact.html" class="hover:text-blue-400">Contact</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </footer>
    </div>
</body>
</html>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Signature Creator</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            margin: 0;
            padding: 20px;
            background-color: #f5f7fa;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .header h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #7f8c8d;
        }
        
        .signature-container {
            width: 100%;
            max-width: 800px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 20px;
        }
        
        .canvas-wrapper {
            position: relative;
            width: 100%;
            height: 200px;
            border: 1px dashed #ccc;
            margin-bottom: 20px;
        }
        
        #signatureCanvas {
            width: 100%;
            height: 100%;
            background-color: #fff;
            cursor: crosshair;
        }
        
        .tools {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .color-picker, .pen-size {
            display: flex;
            align-items: center;
        }
        
        .color-picker label, .pen-size label {
            margin-right: 10px;
            color: #2c3e50;
            font-weight: 500;
        }
        
        #penColor {
            width: 40px;
            height: 40px;
            border: none;
            cursor: pointer;
        }
        
        #penSize {
            width: 80px;
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .clear-btn {
            background-color: #e74c3c;
            color: white;
        }
        
        .clear-btn:hover {
            background-color: #c0392b;
        }
        
        .save-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .save-btn:hover {
            background-color: #27ae60;
        }
        
        .upload-btn {
            background-color: #3498db;
            color: white;
        }
        
        .upload-btn:hover {
            background-color: #2980b9;
        }
        
        .instructions {
            margin-top: 30px;
            background-color: #e8f4f8;
            padding: 15px;
            border-radius: 8px;
            color: #2c3e50;
            width: 100%;
            max-width: 800px;
        }
        
        .instructions h3 {
            margin-top: 0;
            color: #3498db;
        }
        
        .file-input {
            display: none;
        }
        
        .placeholder-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #bdc3c7;
            pointer-events: none;
        }
        
        @media (max-width: 600px) {
            .tools {
                flex-direction: column;
            }
            
            .action-buttons {
                flex-direction: column;
            }
            
            button {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Digital Signature Creator</h1>
        <p>Create or upload your digital signature</p>
    </div>
    
    <div class="signature-container">
        <div class="canvas-wrapper">
            <canvas id="signatureCanvas"></canvas>
            <div class="placeholder-text">Draw your signature here</div>
        </div>
        
        <div class="tools">
            <div class="color-picker">
                <label for="penColor">Pen Color:</label>
                <input type="color" id="penColor" value="#000000">
            </div>
            
            <div class="pen-size">
                <label for="penSize">Pen Size:</label>
                <input type="range" id="penSize" min="1" max="10" value="2">
            </div>
        </div>
        
        <div class="action-buttons">
            <button class="clear-btn" id="clearBtn">Clear Signature</button>
            <button class="save-btn" id="saveBtn">Save Signature</button>
            <button class="upload-btn" id="uploadBtn">Upload Signature</button>
            <input type="file" id="fileInput" class="file-input" accept="image/*">
        </div>
    </div>
    
    <div class="instructions">
        <h3>How to use:</h3>
        <ol>
            <li>Draw your signature in the canvas area using your mouse or touch screen</li>
            <li>Adjust pen color and thickness using the tools above</li>
            <li>Click "Clear Signature" to start over</li>
            <li>Click "Save Signature" to download your signature as PNG</li>
            <li>Click "Upload Signature" to upload an existing signature image</li>
        </ol>
    </div>
    
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const canvas = document.getElementById('signatureCanvas');
            const ctx = canvas.getContext('2d');
            const placeholderText = document.querySelector('.placeholder-text');
            const penColor = document.getElementById('penColor');
            const penSize = document.getElementById('penSize');
            const clearBtn = document.getElementById('clearBtn');
            const saveBtn = document.getElementById('saveBtn');
            const uploadBtn = document.getElementById('uploadBtn');
            const fileInput = document.getElementById('fileInput');
            
            let isDrawing = false;
            let lastX = 0;
            let lastY = 0;
            
            // Set canvas size
            function resizeCanvas() {
                const rect = canvas.parentElement.getBoundingClientRect();
                canvas.width = rect.width;
                canvas.height = rect.height;
                canvas.style.width = rect.width + 'px';
                canvas.style.height = rect.height + 'px';
            }
            
            // Initial resize
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // Drawing functions
            function startDrawing(e) {
                isDrawing = true;
                [lastX, lastY] = getCoordinates(e);
                placeholderText.style.display = 'none';
            }
            
            function draw(e) {
                if (!isDrawing) return;
                
                ctx.strokeStyle = penColor.value;
                ctx.lineWidth = penSize.value;
                ctx.lineJoin = 'round';
                ctx.lineCap = 'round';
                
                const [x, y] = getCoordinates(e);
                
                ctx.beginPath();
                ctx.moveTo(lastX, lastY);
                ctx.lineTo(x, y);
                ctx.stroke();
                
                [lastX, lastY] = [x, y];
            }
            
            function stopDrawing() {
                isDrawing = false;
            }
            
            function getCoordinates(e) {
                let x, y;
                if (e.type.includes('touch')) {
                    x = e.touches[0].clientX - canvas.getBoundingClientRect().left;
                    y = e.touches[0].clientY - canvas.getBoundingClientRect().top;
                } else {
                    x = e.offsetX;
                    y = e.offsetY;
                }
                return [x, y];
            }
            
            // Event listeners for drawing
            canvas.addEventListener('mousedown', startDrawing);
            canvas.addEventListener('mousemove', draw);
            canvas.addEventListener('mouseup', stopDrawing);
            canvas.addEventListener('mouseout', stopDrawing);
            
            // Touch support
            canvas.addEventListener('touchstart', function(e) {
                e.preventDefault();
                startDrawing(e);
            });
            
            canvas.addEventListener('touchmove', function(e) {
                e.preventDefault();
                draw(e);
            });
            
            canvas.addEventListener('touchend', stopDrawing);
            
            // Clear canvas
            clearBtn.addEventListener('click', function() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                placeholderText.style.display = 'block';
            });
            
            // Save signature
            saveBtn.addEventListener('click', function() {
                if (isCanvasEmpty(canvas)) {
                    alert('Please create a signature first');
                    return;
                }
                
                const link = document.createElement('a');
                link.download = 'signature.png';
                link.href = canvas.toDataURL('image/png');
                link.click();
            });
            
            // Upload signature
            uploadBtn.addEventListener('click', function() {
                fileInput.click();
            });
            
            fileInput.addEventListener('change', function(e) {
                if (e.target.files && e.target.files[0]) {
                    const reader = new FileReader();
                    
                    reader.onload = function(event) {
                        const img = new Image();
                        img.onload = function() {
                            // Clear canvas
                            ctx.clearRect(0, 0, canvas.width, canvas.height);
                            placeholderText.style.display = 'none';
                            
                            // Calculate dimensions to fit the canvas while maintaining aspect ratio
                            const scale = Math.min(
                                canvas.width / img.width,
                                canvas.height / img.height
                            );
                            const width = img.width * scale;
                            const height = img.height * scale;
                            const x = (canvas.width - width) / 2;
                            const y = (canvas.height - height) / 2;
                            
                            // Draw the image
                            ctx.drawImage(img, x, y, width, height);
                        };
                        img.src = event.target.result;
                    };
                    
                    reader.readAsDataURL(e.target.files[0]);
                }
            });
            
            // Check if canvas is empty
            function isCanvasEmpty(canvas) {
                const blank = document.createElement('canvas');
                blank.width = canvas.width;
                blank.height = canvas.height;
                return canvas.toDataURL() === blank.toDataURL();
            }
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Employee Termination Letter Generator</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
            color: #333;
        }
        .container {
            max-width: 800px;
            margin: 30px auto;
            background: white;
            padding: 30px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 30px;
            border-bottom: 1px solid #eee;
            padding-bottom: 20px;
        }
        .company-logo {
            text-align: right;
            margin-left: 20px;
        }
        .company-logo img {
            max-width: 150px;
        }
        .employee-photo img {
            max-width: 100px;
            border-radius: 4px;
            border: 1px solid #ddd;
        }
        h1 {
            color: #2c3e50;
            font-size: 24px;
            margin-bottom: 30px;
        }
        .letter-meta {
            margin-bottom: 30px;
        }
        .letter-meta p {
            margin: 5px 0;
        }
        .letter-body {
            margin-bottom: 30px;
        }
        .letter-body p {
            margin-bottom: 15px;
        }
        footer {
            margin-top: 40px;
            border-top: 1px solid #eee;
            padding-top: 20px;
        }
        .signature {
            margin-top: 50px;
        }
        .signature-line {
            width: 300px;
            border-top: 1px solid #333;
            margin-top: 50px;
        }
        .form-container {
            background: #f9f9f9;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 30px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input, textarea, select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
        }
        button {
            background: #2c3e50;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            transition: background 0.3s;
        }
        button:hover {
            background: #1a252f;
        }
        @media print {
            .form-container, button {
                display: none;
            }
            .container {
                box-shadow: none;
                margin: 0;
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="form-container">
            <h1>Termination Letter Generator</h1>
            <div class="form-group">
                <label for="companyName">Company Name</label>
                <input type="text" id="companyName" value="Lavanya Healthcare Limited">
            </div>
            <div class="form-group">
                <label for="companyAddress">Company Address</label>
                <textarea id="companyAddress">Lavanya Healthcare Ltd.
Khewat No. 359/310, Behra Road,
Dera Bassi, Mohali - 140507</textarea>
            </div>
            <div class="form-group">
                <label for="date">Date</label>
                <input type="date" id="date">
            </div>
            <div class="form-group">
                <label for="employeeName">Employee Name</label>
                <input type="text" id="employeeName" value="John Doe">
            </div>
            <div class="form-group">
                <label for="employeeId">Employee ID</label>
                <input type="text" id="employeeId" value="EMP12345">
            </div>
            <div class="form-group">
                <label for="terminationDate">Termination Date</label>
                <input type="date" id="terminationDate">
            </div>
            <div class="form-group">
                <label for="terminationReason">Termination Reason</label>
                <select id="terminationReason">
                    <option value="performance">Performance Issues</option>
                    <option value="layoff">Company Layoff</option>
                    <option value="behavior">Behavioral Issues</option>
                    <option value="attendance">Attendance Problems</option>
                    <option selected value="other">Other</option>
                </select>
            </div>
            <button onclick="generateLetter()">Generate Termination Letter</button>
        </div>

        <div id="letterContainer">
            <header>
                <div>
                    <h1>TERMINATION LETTER</h1>
                    <div class="letter-meta">
                        <p id="outputDate"></p>
                        <p id="outputEmployeeInfo"></p>
                    </div>
                </div>
                <div class="company-logo">
                    <img src="https://placehold.co/300x100?text=Company+Logo" alt="Lavanya Healthcare Limited logo with blue and white theme" />
                </div>
            </header>

            <div class="letter-body">
                <p>Dear <span id="outputName">Employee Name</span>,</p>
                
                <p>The management of Lavanya Healthcare Limited reserves the right to terminate the employment of any employee, staff member, or worker with immediate effect on the grounds of severe misconduct or indisciplinary actions. Such grounds include, but are not limited to: <span id="outputCompanyName">[Company Name]</span>, effective <span id="outputTerminationDate">[Termination Date]</span>. This decision has been made after careful consideration.</p>
                
                <p>Causing substantial financial loss or damage to the company:<span id="outputTerminationReason">[Reason]</span>.</p>
                
                <div class="employee-section">
                    
                    </div>
                </div>
                
                <p>Employees found involved in any of the above or related activities will be subject to immediate termination, without any prior notice, and such termination shall be considered final and binding.

Furthermore, the termination letter issued in such cases will clearly state the misconduct and the reason for termination, serving as an advisory to any future employer. This letter will outline the behavioral and professional concerns observed, and acts as a formal caution for any organization that considers hiring such individuals. If any company chooses to employ the said individual despite such advisory, they do so at their own discretion and risk.

This termination will also result in the blacklisting of the individual within our company records and affiliated networks, and no future employment consideration shall be entertained under any circumstances.
</p>
                
                <p>Creating disruptions or unrest among employees or attempting to disturb workplace peace;
 <span id="outputCompanyName2">[Lavanya Healthcare Limited]</span> Displaying disrespectful behavior towards juniors, colleagues, or seniors;
</p>
                
                <p>Should you have any questions regarding your termination or benefits, please contact Human Resources at Lavanyahealthcarehr@gmail.com</p>
                
                <p>Sincerely,</p>
                
                <div class="signature">
                    <div class="signature-line"></div>
                    <p>[Authorized Signatory]</p>
                    <p>Human Resources Manager</p>
                    <p><span id="outputCompanyName3">[Lavanya Healthcare limited]</span></p>
                </div>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Set default dates
            const today = new Date();
            document.getElementById('date').valueAsDate = today;
            
            const terminationDate = new Date();
            terminationDate.setDate(today.getDate() + 14); // 2 weeks notice
            document.getElementById('terminationDate').valueAsDate = terminationDate;
            
            // Generate initial letter with defaults
            generateLetter();
        });

        function generateLetter() {
            // Get form values
            const companyName = document.getElementById('companyName').value;
            const companyAddress = document.getElementById('companyAddress').value;
            const date = new Date(document.getElementById('date').value);
            const employeeName = document.getElementById('employeeName').value;
            const employeeId = document.getElementById('employeeId').value;
            const terminationDate = new Date(document.getElementById('terminationDate').value);
            const terminationReason = document.getElementById('terminationReason').value;
            
            // Format dates
            const formattedDate = formatDate(date);
            const formattedTerminationDate = formatDate(terminationDate);
            
            // Map reason to text
            const reasonText = {
                'performance': 'unsatisfactory work performance',
                'layoff': 'company restructuring and position elimination',
                'behavior': 'violation of company policies',
                'attendance': 'continued attendance problems',
                'other': ''
            }[terminationReason];
            
            // Update letter output
            document.getElementById('outputDate').textContent = formattedDate;
            document.getElementById('outputEmployeeInfo').textContent = employeeName + " (ID: " + employeeId + ")";
            document.getElementById('outputName').textContent = employeeName;
            document.getElementById('outputCompanyName').textContent = companyName;
            document.getElementById('outputCompanyName2').textContent = companyName;
            document.getElementById('outputCompanyName3').textContent = companyName;
            document.getElementById('outputTerminationDate').textContent = formattedTerminationDate;
            document.getElementById('outputTerminationReason').textContent = reasonText;
            document.getElementById('outputEmpId').textContent = employeeId;
            
            // Update employee photo alt text
            const employeePhoto = document.getElementById('employeePhoto');
            employeePhoto.alt = "Photo of employee " + employeeName;
        }

        function formatDate(date) {
            if (!date) return "[Date]";
            
            const options = { year: 'numeric', month: 'long', day: 'numeric' };
            return date.toLocaleDateString('en-US', options);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Lavanya Healthcare Employee Registration</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @media print {
            .no-print { display: none; }
            .print-section { box-shadow: none!important; }
        }
    </style>
</head>
<body class="bg-blue-50 min-h-screen flex flex-col items-center py-8">

<div class="bg-white shadow-lg rounded-xl p-8 w-full max-w-2xl mt-6 relative print-section">
    <h1 class="text-2xl font-bold text-center text-blue-800 mb-6">Employee Onboarding - Lavanya Healthcare Ltd.</h1>
    <form id="empForm" class="space-y-4 mb-8 no-print">
        <div>
            <label class="block text-gray-700 font-medium mb-1">Employee Name</label>
            <input type="text" id="empName" class="w-full border rounded px-2 py-2" required>
        </div>
        <div>
            <label class="block text-gray-700 font-medium mb-1">Department</label>
            <input type="text" id="empDept" class="w-full border rounded px-2 py-2" required>
        </div>
        <div>
            <label class="block text-gray-700 font-medium mb-1">Designation</label>
            <input type="text" id="empDesig" class="w-full border rounded px-2 py-2" required>
        </div>
        <div>
            <label class="block text-gray-700 font-medium mb-1">Mobile Number</label>
            <input type="tel" id="empMobile" class="w-full border rounded px-2 py-2" required pattern="[0-9]{10}">
        </div>
        <div>
            <label class="block text-gray-700 font-medium mb-1">Gmail ID</label>
            <input type="email" id="empGmail" class="w-full border rounded px-2 py-2" required pattern=".+@gmail\.com">
        </div>
        <div class="flex justify-center gap-4 pt-4">
            <button type="submit" class="bg-blue-600 hover:bg-blue-700 text-white rounded px-5 py-2 font-medium">Add Employee</button>
            <button type="reset" class="bg-gray-300 hover:bg-gray-400 rounded px-4 py-2 font-medium text-gray-800">Reset</button>
        </div>
    </form>

    <!-- Result Section -->
    <section id="resultSection" class="hidden">
        <div class="bg-green-50 p-6 rounded shadow">
            <div class="mb-4">
                <h2 class="text-xl font-semibold text-green-700 mb-2">Employee Registered Successfully!</h2>
                <p><strong>Name:</strong> <span id="showName"></span></p>
                <p><strong>Department:</strong> <span id="showDept"></span></p>
                <p><strong>Designation:</strong> <span id="showDesig"></span></p>
            </div>
            <hr class="my-4">
            <h3 class="text-lg font-medium text-blue-700">Auto Credentials</h3>
            <ul class="mb-4 text-base text-gray-800">
                <li><strong>Employee ID (EmpID):</strong> <span id="showEmpID"></span></li>
                <li><strong>Login ID:</strong> <span id="showLoginID"></span></li>
                <li><strong>Password:</strong> <span id="showPassword"></span></li>
            </ul>
            <hr class="my-4">
            <div class="mb-2">
                <strong>To send via SMS/email:</strong>
                <div class="text-sm bg-gray-100 p-2 rounded">
                    Dear <span id="smsName"></span>,<br>
                    Your Emp ID: <span id="smsEmpID"></span><br>
                    Login ID: <span id="smsLoginID"></span><br>
                    Password: <span id="smsPassword"></span><br>
                    -- Team Lavanya Healthcare
                </div>
            </div>
            <div class="flex gap-4 mt-6 no-print">
                <button onclick="window.print()" class="bg-green-600 hover:bg-green-700 text-white px-6 py-2 rounded font-medium">Print</button>
                <button onclick="window.location.reload()" class="bg-gray-400 hover:bg-gray-600 text-white px-5 py-2 rounded font-medium">Add Another</button>
            </div>
        </div>
    </section>
</div>

<script>
/* Store last used EmpID/Counter in localStorage for persistence */
function getLastEmpNo() {
    return Number(localStorage.getItem('LHL_LastEmpNo') || 0);
}
function setLastEmpNo(n) {
    localStorage.setItem('LHL_LastEmpNo', n);
}

// Pad with leading zeros, e.g., "001" for 1
function pad(num, size) {
    let s = num+"";
    while (s.length < size) s = "0" + s;
    return s;
}

function generateEmpID() {
    let nextNo = getLastEmpNo() + 1;
    if(nextNo > 10000) nextNo = 1;
    setLastEmpNo(nextNo);
    return "LHL" + pad(nextNo, 3);   // LHL001, LHL002, ...
}

// Simple user login ID: e.g., first name + last 3 mobile + last 2 EmpID digits
function generateLoginID(name, empID, mobile) {
    let first = name.split(" ")[0].toLowerCase();
    let mobilePart = mobile.slice(-3);
    let empSuffix = empID.slice(-2);
    return first + mobilePart + empSuffix;
}

// Strong random 8-char password
function randomPassword(len=8) {
    const chars = "ABCDEFGHJKLMNPQRSTUVWXYZabcdefghijkmnopqrstuvwxyz23456789!@#";
    let pwd = "";
    for(let i=0; i<len; ++i)
        pwd += chars[Math.floor(Math.random()*chars.length)];
    return pwd;
}

const form = document.getElementById("empForm");
form.onsubmit = function(e){
    e.preventDefault();
    let name = document.getElementById("empName").value.trim();
    let dept = document.getElementById("empDept").value.trim();
    let desig = document.getElementById("empDesig").value.trim();
    let mobile = document.getElementById("empMobile").value.trim();
    let gmail = document.getElementById("empGmail").value.trim();

    if(!name || !dept || !desig || !mobile.match(/^[0-9]{10}$/) || !gmail.match(/@gmail\.com$/i)) {
        alert("Please provide all info with valid mobile and Gmail.");
        return;
    }

    // Generate credentials
    let empID = generateEmpID();
    let loginID = generateLoginID(name, empID, mobile);
    let pwd = randomPassword();

    // Show on page
    document.getElementById("showName").textContent = name;
    document.getElementById("showDept").textContent = dept;
    document.getElementById("showDesig").textContent = desig;
    document.getElementById("showEmpID").textContent = empID;
    document.getElementById("showLoginID").textContent = loginID;
    document.getElementById("showPassword").textContent = pwd;
    document.getElementById("smsName").textContent = name.split(" ")[0];
    document.getElementById("smsEmpID").textContent = empID;
    document.getElementById("smsLoginID").textContent = loginID;
    document.getElementById("smsPassword").textContent = pwd;

    // Hide form, show result
    form.classList.add("hidden");
    document.getElementById("resultSection").classList.remove("hidden");

    // Simulate sending SMS/Email (for real-world use, connect to backend API)
    // e.g., call fetch('/api/send_sms', {body: ...}) and send email similarly.
};
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Attendance</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        table {
            border-collapse: separate;
            border-spacing: 0;
        }
        th, td {
            border-bottom: 1px solid #e5e7eb;
        }
        tr:hover {
            background-color: #f9fafb;
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="Home.html" class="px-3 py-2 rounded hover:bg-blue-500">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="Attandance.html" class="px-3 py-2 rounded active">Attendance</a></li>
                      <li><a href="New Hire.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header>

        <!-- Main Content -->
        <main class="flex-grow container mx-auto px-4 py-8">
            <div class="flex justify-between items-center mb-8">
                <h2 class="text-2xl font-bold text-gray-800">Attendance Records</h2>
                <div class="flex space-x-4">
                    <button class="bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 rounded-lg flex items-center">
                        <img src="https://placehold.co/20x20" alt="Calendar icon for generating attendance report" class="mr-2"> Generate Report
                    </button>
                    <button class="border border-blue-600 text-blue-600 hover:bg-blue-50 px-4 py-2 rounded-lg flex items-center">
                        <img src="https://placehold.co/20x20" alt="Clock icon representing manual attendance entry" class="mr-2"> Manual Entry
                    </button>
                </div>
            </div>

            <div class="bg-white rounded-lg shadow-md overflow-hidden mb-6">
                <div class="p-4 border-b">
                    <div class="flex flex-wrap justify-between items-center">
                        <div class="mb-4 md:mb-0">
                            <label class="block text-gray-700 mb-1">Date Range</label>
                            <div class="flex space-x-2">
                                <input type="date" class="border rounded-lg px-3 py-2">
                                <span class="flex items-center">to</span>
                                <input type="date" class="border rounded-lg px-3 py-2">
                            </div>
                        </div>
                        <div>
                            <label class="block text-gray-700 mb-1">Department</label>
                            <select class="border rounded-lg px-3 py-2">
                                <option>All Departments</option>
                                <option>IT</option>
                                <option>HR</option>
                                <option>Finance</option>
                                <option>Operations</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-gray-700 mb-1">Status</label>
                            <select class="border rounded-lg px-3 py-2">
                                <option>All Status</option>
                                <option>Present</option>
                                <option>Absent</option>
                                <option>Late</option>
                                <option>On Leave</option>
                            </select>
                        </div>
                    </div>
                </div>
                
                <div class="overflow-x-auto">
                    <table class="w-full">
                        <thead class="bg-gray-50">
                            <tr class="text-left text-gray-500">
                                <th class="px-6 py-3">Date</th>
                                <th class="px-6 py-3">Employee ID</th>
                                <th class="px-6 py-3">Name</th>
                                <th class="px-6 py-3">Check In</th>
                                <th class="px-6 py-3">Check Out</th>
                                <th class="px-6 py-3">Working Hours</th>
                                <th class="px-6 py-3">Status</th>
                                <th class="px-6 py-3">Remarks</th>
                            </tr>
                        </thead>
                        <tbody class="text-gray-700">
                            <tr>
                                <td class="px-6 py-4">15 Jun 2023</td>
                                <td class="px-6 py-4">EMP001</td>
                                <td class="px-6 py-4">John Doe</td>
                                <td class="px-6 py-4">08:45 AM</td>
                                <td class="px-6 py-4">05:30 PM</td>
                                <td class="px-6 py-4">8.5 hrs</td>
                                <td class="px-6 py-4"><span class="bg-green-100 text-green-800 px-2 py-1 rounded-full text-xs">Present</span></td>
                                <td class="px-6 py-4">-</td>
                            </tr>
                            <tr>
                                <td class="px-6 py-4">15 Jun 2023</td>
                                <td class="px-6 py-4">EMP002</td>
                                <td class="px-6 py-4">Jane Smith</td>
                                <td class="px-6 py-4">09:15 AM</td>
                                <td class="px-6 py-4">05:45 PM</td>
                                <td class="px-6 py-4">8.5 hrs</td>
                                <td class="px-6 py-4"><span class="bg-yellow-100 text-yellow-800 px-2 py-1 rounded-full text-xs">Late</span></td>
                                <td class="px-6 py-4">Traffic delay</td>
                            </tr>
                            <tr>
                                <td class="px-6 py-4">15 Jun 2023</td>
                                <td class="px-6 py-4">EMP003</td>
                                <td class="px-6 py-4">Robert Johnson</td>
                                <td class="px-6 py-4">-</td>
                                <td class="px-6 py-4">-</td>
                                <td class="px-6 py-4">0 hrs</td>
                                <td class="px-6 py-4"><span class="bg-red-100 text-red-800 px-2 py-1 rounded-full text-xs">Absent</span></td>
                                <td class="px-6 py-4">Sick Leave</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <div class="p-4 border-t flex justify-between items-center">
                    <div class="text-gray-500">
                        Showing 1 to 3 of 45 entries
                    </div>
                    <div class="flex space-x-2">
                        <button class="px-3 py-1 border rounded-md">Previous</button>
                        <button class="px-3 py-1 border rounded-md bg-blue-600 text-white">1</button>
                        <button class="px-3 py-1 border rounded-md">2</button>
                        <button class="px-3 py-1 border rounded-md">3</button>
                        <button class="px-3 py-1 border rounded-md">Next</button>
                    </div>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-lg font-semibold text-gray-800 mb-4">Attendance Overview</h3>
                    <div class="space-y-4">
                        <div class="flex justify-between">
                            <span class="text-gray-600">Total Employees</span>
                            <span class="font-semibold">42</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-gray-600">Present Today</span>
                            <span class="font-semibold">38</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-gray-600">Absent Today</span>
                            <span class="font-semibold">3</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-gray-600">Late Today</span>
                            <span class="font-semibold">1</span>
                        </div>
                    </div>
                </div>

                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-lg font-semibold text-gray-800 mb-4">Attendance Stats</h3>
                    <div class="flex justify-center mb-4">
                        <img src="https://placehold.co/200x200" alt="Donut chart showing attendance percentage breakdown with present, absent and late categories" class="w-40 h-40">
                    </div>
                    <div class="space-y-2">
                        <div class="flex items-center">
                            <span class="w-3 h-3 bg-green-500 rounded-full mr-2"></span>
                            <span class="text-gray-600 text-sm">Present (90.5%)</span>
                        </div>
                        <div class="flex items-center">
                            <span class="w-3 h-3 bg-yellow-500 rounded-full mr-2"></span>
                            <span class="text-gray-600 text-sm">Late (2.4%)</span>
                        </div>
                        <div class="flex items-center">
                            <span class="w-3 h-3 bg-red-500 rounded-full mr-2"></span>
                            <span class="text-gray-600 text-sm">Absent (7.1%)</span>
                        </div>
                    </div>
                </div>

                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-lg font-semibold text-gray-800 mb-4">Monthly Trend</h3>
                    <div class="flex justify-center mb-4">
                        <img src="https://placehold.co/200x100" alt="Bar chart showing monthly attendance percentage trends with increasing bars" class="w-full h-32">
                    </div>
                    <div class="text-center text-gray-600 text-sm">
                        Monthly attendance percentage trend
                    </div>
                </div>
            </div>
        </main>

        <!-- Footer -->
        <footer class="bg-gray-800 text-white py-8">
            <div class="container mx-auto px-4">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <div class="mb-4 md:mb-0">
                        <h3 class="text-xl font-bold mb-2">HR Dashboard</h3>
                        <p class="text-gray-400">© 2023 Company Name. All rights reserved.</p>
                    </div>
                    <nav>
                        <ul class="flex space-x-6">
                            <li><a href="index.html" class="hover:text-blue-400">Home</a></li>
                            <li><a href="privacy.html" class="hover:text-blue-400">Privacy Policy</a></li>
                            <li><a href="terms.html" class="hover:text-blue-400">Terms</a></li>
                            <li><a href="contact.html" class="hover:text-blue-400">Contact</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </footer>
    </div>
</body>
</html>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="New hire.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Innovatek - Employee Portal</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root {
            --primary: #3b82f6;
            --secondary: #10b981;
            --dark: #1e293b;
            --light: #f8fafc;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f1f5f9;
        }
        
        .employee-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .value-card {
            transition: all 0.3s ease;
        }
        
        .value-card:hover {
            background-color: rgba(255, 255, 255, 0.8);
        }
        
        #searchResults {
            max-height: 300px;
            overflow-y: auto;
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <div class="bg-gradient-to-r from-blue-600 to-blue-800 text-white">
        <div class="max-w-7xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:px-8 text-center">
            <h1 class="text-4xl md:text-5xl font-bold mb-6">Meet Our Team</h1>
            <p class="text-xl md:text-2xl max-w-3xl mx-auto">
                Passionate professionals dedicated to innovation and excellence.
            </p>
            <div class="mt-10 flex justify-center space-x-4">
                <a href="#directory" class="bg-white text-blue-600 px-6 py-3 rounded-md font-medium hover:bg-gray-100 transition duration-300">
                    Find a Colleague
                </a>
                <a href="#values" class="bg-blue-700 text-white px-6 py-3 rounded-md font-medium hover:bg-blue-800 transition duration-300">
                    Our Culture
                </a>
            </div>
        </div>
    </div>
    
    <!-- Featured Employees -->
    <section id="employees" class="py-16 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-900 mb-4">Featured Employees</h2>
                <p class="text-lg text-gray-600 max-w-2xl mx-auto">
                    Get to know some of the talented individuals who make our company great.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Employee 1 -->
                <div class="employee-card bg-white rounded-xl shadow-md overflow-hidden transition duration-300">
                    <div class="h-48 bg-gradient-to-r from-blue-500 to-blue-700 flex items-center justify-center">
                        <img src="https://placehold.co/300x300" alt="Portrait of Sarah Johnson, Senior Developer with short brown hair and glasses, smiling professionally" class="h-40 w-40 rounded-full border-4 border-white">
                    </div>
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-bold text-gray-900 mb-1">Sarah Johnson</h3>
                        <p class="text-blue-600 font-medium">Senior Developer</p>
                        <p class="text-gray-600 mt-3">Leads our engineering team with expertise in JavaScript and cloud architecture.</p>
                        <div class="mt-4 flex justify-center space-x-3">
                            <span class="bg-blue-100 text-blue-800 text-xs px-2 py-1 rounded">JavaScript</span>
                            <span class="bg-green-100 text-green-800 text-xs px-2 py-1 rounded">React</span>
                            <span class="bg-purple-100 text-purple-800 text-xs px-2 py-1 rounded">Cloud</span>
                        </div>
                    </div>
                </div>
                
                <!-- Employee 2 -->
                <div class="employee-card bg-white rounded-xl shadow-md overflow-hidden transition duration-300">
                    <div class="h-48 bg-gradient-to-r from-green-500 to-green-700 flex items-center justify-center">
                        <img src="https://placehold.co/300x300" alt="Portrait of Michael Chen, Marketing Director with dark hair and blue shirt, looking confident" class="h-40 w-40 rounded-full border-4 border-white">
                    </div>
                    <div class="p-6 text-center">
                        
                        <p class="text-gray-600 mt-3">Drives our brand strategy and digital marketing initiatives.</p>
                        <div class="mt-4 flex justify-center space-x-3">
                            <span class="bg-yellow-100 text-yellow-800 text-xs px-2 py-1 rounded">Strategy</span>
                            <span class="bg-pink-100 text-pink-800 text-xs px-2 py-1 rounded">Branding</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs px-2 py-1 rounded">SEO</span>
                        </div>
                    </div>
                </div>
                
                <!-- Employee 3 -->
                <div class="employee-card bg-white rounded-xl shadow-md overflow-hidden transition duration-300">
                    <div class="h-48 bg-gradient-to-r from-purple-500 to-purple-700 flex items-center justify-center">
                        <img src="https://placehold.co/300x300" alt="Portrait of David Ramirez, Product Manager with beard smiling casually in a meeting room" class="h-40 w-40 rounded-full border-4 border-white">
                    </div>
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-bold text-gray-900 mb-1">David Ramirez</h3>
                        <p class="text-purple-600 font-medium">Product Manager</p>
                        <p class="text-gray-600 mt-3">Bridges user needs with technical solutions for impactful products.</p>
                        <div class="mt-4 flex justify-center space-x-3">
                            <span class="bg-red-100 text-red-800 text-xs px-2 py-1 rounded">UX</span>
                            <span class="bg-teal-100 text-teal-800 text-xs px-2 py-1 rounded">Agile</span>
                            <span class="bg-orange-100 text-orange-800 text-xs px-2 py-1 rounded">Analytics</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Company Values -->
    <section id="values" class="py-16 px-4 sm:px-6 lg:px-8 bg-gray-50">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-900 mb-4">Our Core Values</h2>
                <p class="text-lg text-gray-600 max-w-2xl mx-auto">
                    The principles that guide every decision we make and action we take.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Value 1 -->
                <div class="value-card bg-white p-8 rounded-lg shadow-sm hover:shadow-md transition duration-300">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-gray-900 mb-3">Innovation</h3>
                    <p class="text-gray-600">We embrace curiosity and champion new ideas that push boundaries and create lasting impact.</p>
                </div>
                
                <!-- Value 2 -->
                <div class="value-card bg-white p-8 rounded-lg shadow-sm hover:shadow-md transition duration-300">
                    <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mb-6">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z" />
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-gray-900 mb-3">Collaboration</h3>
                    <p class="text-gray-600">We believe our diverse talents create better solutions when we work together with trust and respect.</p>
                </div>
                
                <!-- Value 3 -->
                <div class="value-card bg-white p-8 rounded-lg shadow-sm hover:shadow-md transition duration-300">
                    <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mb-6">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-gray-900 mb-3">Integrity</h3>
                    <p class="text-gray-600">We foster trust through transparency, honesty, and ethical conduct in all we do.</p>
                </div>
                
                <!-- Value 4 -->
                <div class="value-card bg-white p-8 rounded-lg shadow-sm hover:shadow-md transition duration-300">
                    <div class="w-16 h-16 bg-yellow-100 rounded-full flex items-center justify-center mb-6">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-yellow-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-gray-900 mb-3">Excellence</h3>
                    <p class="text-gray-600">We take pride in our work and strive for the highest quality in everything we deliver.</p>
                </div>
                
                <!-- Value 5 -->
                <div class="value-card bg-white p-8 rounded-lg shadow-sm hover:shadow-md transition duration-300">
                    <div class="w-16 h-16 bg-teal-100 rounded-full flex items-center justify-center mb-6">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-teal-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 4v16M17 4v16M3 8h4m10 0h4M3 12h18M3 16h4m10 0h4M4 20h16a1 1 0 001-1V5a1 1 0 00-1-1H4a1 1 0 00-1 1v14a1 1 0 001 1z" />
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-gray-900 mb-3">Learning</h3>
                    <p class="text-gray-600">We cultivate continuous growth through feedback, mentorship, and challenging opportunities.</p>
                </div>
                
                <!-- Value 6 -->
                <div class="value-card bg-white p-8 rounded-lg shadow-sm hover:shadow-md transition duration-300">
                    <div class="w-16 h-16 bg-red-100 rounded-full flex items-center justify-center mb-6">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-red-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-gray-900 mb-3">Impact</h3>
                    <p class="text-gray-600">We measure success by the positive difference we make for our customers and communities.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Employee Directory -->
    <section id="directory" class="py-16 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-900 mb-4">Employee Directory</h2>
                <p class="text-lg text-gray-600 max-w-2xl mx-auto">
                    Connect with colleagues across departments and locations.
                </p>
            </div>
            
            <div class="max-w-3xl mx-auto">
                <div class="relative">
                    <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                        <svg class="h-5 w-5 text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd" />
                        </svg>
                    </div>
                    <input type="text" id="searchInput" class="block w-full pl-10 pr-3 py-4 border border-gray-300 rounded-lg bg-gray-50 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500" placeholder="Search by name, department, or skill...">
                </div>
                
                <div id="searchResults" class="mt-6 hidden">
                    <ul class="divide-y divide-gray-200">
                        <!-- Results will be inserted here by JavaScript -->
                    </ul>
                </div>
                
                <div id="allEmployees" class="mt-12">
                    <h3 class="text-xl font-semibold text-gray-900 mb-6">All Employees</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- Departments will be inserted here by JavaScript -->
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Contact Section -->
    <section id="contact" class="py-16 px-4 sm:px-6 lg:px-8 bg-gray-100">
        <div class="max-w-7xl mx-auto">
            <div class="bg-white rounded-xl shadow-md overflow-hidden">
                <div class="md:flex">
                    <div class="md:w-1/2 bg-gradient-to-br from-blue-600 to-blue-800 p-12 text-white">
                        <h2 class="text-3xl font-bold mb-6">Get In Touch</h2>
                        <p class="mb-8 text-blue-100">
                            Have questions about our team or want to learn more about working with us?
                        </p>
                        <div class="space-y-6">
                            <div class="flex items-start">
                                <div class="flex-shrink-0">
                                    <svg class="h-6 w-6 text-blue-300" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                                    </svg>
                                </div>
                                <div class="ml-3">
                                    <p class="text-sm font-medium text-blue-200">Email us</p>
                                    <p class="text-blue-100">Ittechnicianhealthcare@gmail.com</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="flex-shrink-0">
                                    <svg class="h-6 w-6 text-blue-300" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                                    </svg>
                                </div>
                                <div class="ml-3">
                                    <p class="text-sm font-medium text-blue-200">Call us</p>
                                    <p class="text-blue-100">+1 (555) 123-4567</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="flex-shrink-0">
                                    <svg class="h-6 w-6 text-blue-300" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                                    </svg>
                                </div>
                                <div class="ml-3">
                                    <p class="text-sm font-medium text-blue-200">Visit us</p>
                                    <p class="text-blue-100">123 Tech Boulevard, Silicon Valley, CA</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="md:w-1/2 p-12">
                        <h3 class="text-xl font-bold text-gray-900 mb-6">Send us a message</h3>
                        <form class="space-y-6">
                            <div>
                                <label for="name" class="block text-sm font-medium text-gray-700 mb-1">Your Name</label>
                                <input type="text" id="name" class="block w-full px-4 py-3 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                            </div>
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email Address</label>
                                <input type="email" id="email" class="block w-full px-4 py-3 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                            </div>
                            <div>
                                <label for="subject" class="block text-sm font-medium text-gray-700 mb-1">Subject</label>
                                <select id="subject" class="block w-full px-4 py-3 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                                    <option>General Inquiry</option>
                                    <option>Career Opportunities</option>
                                    <option>Press/Media</option>
                                    <option>Partnerships</option>
                                </select>
                            </div>
                            <div>
                                <label for="message" class="block text-sm font-medium text-gray-700 mb-1">Message</label>
                                <textarea id="message" rows="4" class="block w-full px-4 py-3 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500"></textarea>
                            </div>
                            <div>
                                <button type="submit" class="w-full flex justify-center py-3 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-blue-600 hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500 transition duration-300">
                                    Send Message
                                </button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="md:flex md:items-center md:justify-between">
                <div class="flex justify-center md:justify-start">
                    <img src="https://placehold.co/150x50" alt="Innovatek company logo white version with modern minimalist design" class="h-10">
                </div>
                <div class="mt-8 md:mt-0">
                    <div class="flex justify-center md:justify-end space-x-6">
                        <a href="#" class="text-gray-400 hover:text-white">
                            <span class="sr-only">LinkedIn</span>
                            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                                <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <span class="sr-only">Twitter</span>
                            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                                <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z" />
                            </svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <span class="sr-only">GitHub</span>
                            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                                <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" />
                            </svg>
                        </a>
                    </div>
                </div>
            </div>
            <div class="mt-8 border-t border-gray-800 pt-8 md:flex md:items-center md:justify-between">
                <div class="text-center md:text-left">
                    <p class="text-sm text-gray-400">
                        &copy; 2023 Innovatek, Inc. All rights reserved.
                    </p>
                </div>
                <div class="mt-4 md:mt-0">
                    <div class="flex justify-center md:justify-end space-x-6">
                        <a href="#" class="text-sm text-gray-400 hover:text-white">Privacy Policy</a>
                        <a href="#" class="text-sm text-gray-400 hover:text-white">Terms of Service</a>
                        <a href="#" class="text-sm text-gray-400 hover:text-white">Careers</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
    
    <script>
        // Employee data - in a real app this would come from an API
        const employees = [
            {
                id: 1,
                name: "Sarah Johnson",
                position: "Senior Developer",
                department: "Engineering",
                email: "sarah.johnson@innovatek.com",
                phone: "x1234",
                skills: ["JavaScript", "React", "Cloud"],
                image: "https://placehold.co/300x300"
            },
            {
                id: 2,
                name: "Michael Chen",
                position: "Marketing Director",
                department: "Marketing",
                email: "michael.chen@innovatek.com",
                phone: "x2345",
                skills: ["Strategy", "Branding", "SEO"],
                image: "https://placehold.co/300x300"
            },
            {
                id: 3,
                name: "David Ramirez",
                position: "Product Manager",
                department: "Product",
                email: "david.ramirez@innovatek.com",
                phone: "x3456",
                skills: ["UX", "Agile", "Analytics"],
                image: "https://placehold.co/300x300"
            },
            {
                id: 4,
                name: "Emma Wilson",
                position: "UX Designer",
                department: "Design",
                email: "emma.wilson@innovatek.com",
                phone: "x4567",
                skills: ["UI Design", "Research", "Prototyping"],
                image: "https://placehold.co/300x300"
            },
            {
                id: 5,
                name: "James Peterson",
                position: "Data Scientist",
                department: "Engineering",
                email: "james.peterson@innovatek.com",
                phone: "x5678",
                skills: ["Python", "Machine Learning", "Data Visualization"],
                image: "https://placehold.co/300x300"
            },
            {
                id: 6,
                name: "Lisa Wong",
                position: "HR Manager",
                department: "Human Resources",
                email: "lisa.wong@innovatek.com",
                phone: "x6789",
                skills: ["Recruiting", "Training", "Employee Relations"],
                image: "https://placehold.co/300x300"
            },
            {
                id: 7,
                name: "Robert Turner",
                position: "Finance Director",
                department: "Finance",
                email: "robert.turner@innovatek.com",
                phone: "x7890",
                skills: ["Budgeting", "Forecasting", "Financial Analysis"],
                image: "https://placehold.co/300x300"
            },
            {
                id: 8,
                name: "Amanda Lee",
                position: "Sales Executive",
                department: "Sales",
                email: "amanda.lee@innovatek.com",
                phone: "x8901",
                skills: ["CRM", "Negotiation", "Account Management"],
                image: "https://placehold.co/300x300"
            }
        ];
        
        // Group employees by department
        const employeesByDepartment = {};
        employees.forEach(employee => {
            if (!employeesByDepartment[employee.department]) {
                employeesByDepartment[employee.department] = [];
            }
            employeesByDepartment[employee.department].push(employee);
        });
        
        // Render department sections
        const allEmployeesContainer = document.getElementById('allEmployees');
        const departmentsContainer = allEmployeesContainer.querySelector('div:last-child');
        
        Object.keys(employeesByDepartment).forEach(department => {
            const departmentSection = document.createElement('div');
            departmentSection.className = 'department-section';
            
            const heading = document.createElement('h4');
            heading.className = 'text-lg font-semibold text-gray-800 mb-4';
            heading.textContent = department;
            
            const employeeList = document.createElement('div');
            employeeList.className = 'space-y-4';
            
            employeesByDepartment[department].forEach(employee => {
                const employeeCard = document.createElement('div');
                employeeCard.className = 'bg-gray-50 p-4 rounded-lg flex items-center shadow-sm';
                
                employeeCard.innerHTML = `
                    <div class="flex-shrink-0">
                        <img src="${employee.image}" alt="Portrait of ${employee.name}, ${employee.position} with description varying by employee" class="h-12 w-12 rounded-full">
                    </div>
                    <div class="ml-4">
                        <h5 class="text-base font-medium text-gray-900">${employee.name}</h5>
                        <p class="text-sm text-gray-600">${employee.position}</p>
                        <div class="mt-1 flex items-center text-xs text-gray-500">
                            <svg class="h-3 w-3 mr-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                                <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z" />
                                <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z" />
                            </svg>
                            ${employee.email}
                        </div>
                    </div>
                `;
                
                employeeList.appendChild(employeeCard);
            });
            
            departmentSection.appendChild(heading);
            departmentSection.appendChild(employeeList);
            departmentsContainer.appendChild(departmentSection);
        });
        
        // Search functionality
        const searchInput = document.getElementById('searchInput');
        const searchResults = document.getElementById('searchResults');
        
        searchInput.addEventListener('input', function(e) {
            const searchTerm = e.target.value.toLowerCase();
            
            if (searchTerm.length < 2) {
                searchResults.classList.add('hidden');
                searchResults.innerHTML = '';
                allEmployees.classList.remove('hidden');
                return;
            }
            
            allEmployees.classList.add('hidden');
            searchResults.classList.remove('hidden');
            
            const filteredEmployees = employees.filter(employee => 
                employee.name.toLowerCase().includes(searchTerm) || 
                employee.position.toLowerCase().includes(searchTerm) || 
                employee.department.toLowerCase().includes(searchTerm) ||
                employee.skills.some(skill => skill.toLowerCase().includes(searchTerm))
            );
            
            const resultsList = searchResults.querySelector('ul');
            resultsList.innerHTML = '';
            
            if (filteredEmployees.length === 0) {
                resultsList.innerHTML = '<li class="py-4 text-center text-gray-500">No employees found</li>';
                return;
            }
            
            filteredEmployees.forEach(employee => {
                const listItem = document.createElement('li');
                listItem.className = 'py-4 px-4 hover:bg-gray-50';
                
                listItem.innerHTML = `
                    <div class="flex items-center">
                        <div class="flex-shrink-0">
                            <img src="${employee.image}" alt="Portrait of ${employee.name}, ${employee.position}" class="h-10 w-10 rounded-full">
                        </div>
                        <div class="ml-4">
                            <h4 class="text-sm font-medium text-gray-900">${employee.name}</h4>
                            <p class="text-sm text-gray-500">${employee.position} • ${employee.department}</p>
                            <div class="mt-1 flex space-x-2">
                                ${employee.skills.map(skill => `<span class="inline-flex items-center px-2 py-0.5 rounded text-xs font-medium bg-blue-100 text-blue-800">${skill}</span>`).join('')}
                            </div>
                        </div>
                    </div>
                `;
                
                resultsList.appendChild(listItem);
            });
        });
 <nav class="bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex items-center">
                    <div class="flex-shrink-0">
                        <img src="https://placehold.co/150x50" alt="Innovatek company logo with modern blue gradient design and abstract tech symbol" class="h-10">
                    </div>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#employees" class="text-gray-700 hover:text-blue-600 px-3 py-2 rounded-md text-sm font-medium">Our Team</a>
                        <a href="#values" class="text-gray-700 hover:text-blue-600 px-3 py-2 rounded-md text-sm font-medium">Our Values</a>
                        <a href="#directory" class="text-gray-700 hover:text-blue-600 px-3 py-2 rounded-md text-sm font-medium">Directory</a>
                        <a href="#contact" class="text-gray-700 hover:text-blue-600 px-3 py-2 rounded-md text-sm font-medium">Contact</a>
                    </div>
                </div>
            </div>
        </div>
    </nav>
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Dashboard - Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .active {
            background-color: #3b82f6;
            color: white;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="bg-gray-50">
    <div class="flex flex-col min-h-screen">
        <!-- Header -->
        <header class="bg-blue-600 text-white shadow-lg">
            <div class="container mx-auto px-4 py-4 flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <img src="https://placehold.co/50x50" alt="Company logo with modern blue and white design showing stylized human figures" class="rounded-full">
                    <h1 class="text-2xl font-bold">HR Dashboard</h1>
                </div>
                <nav>
                    <ul class="flex space-x-6">
                        <li><a href="home.html" class="px-3 py-2 rounded active">Home</a></li>
                        <li><a href="employee.html" class="px-3 py-2 rounded hover:bg-blue-500">Employees</a></li>
                        <li><a href="salary.html" class="px-3 py-2 rounded hover:bg-blue-500">Salary</a></li>
                        <li><a href="attandance.html" class="px-3 py-2 rounded hover:bg-blue-500">Attandance</a></li>
                        <li><a href="New Hire.html" class="px-3 py-2 rounded hover:bg-blue-500">New Hire</a></li>
                    </ul>
                </nav>
            </div>
        </header><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LHL Employee Management System</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f5f7fa;
        }
        .id-card {
            width: 85mm;
            height: 54mm;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }
        .id-front {
            background: linear-gradient(135deg, #2563eb 0%, #1e40af 100%);
            color: white;
        }
        .id-back {
            background: white;
            color: #333;
        }
        .photo-circle {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            border: 3px solid white;
            overflow: hidden;
        }
        
    </style>
</head>
<body class="bg-gray-100">
    <div class="container mx-auto px-4 py-8">
        <div class="flex justify-between items-center mb-8">
            <h1 class="text-3xl font-bold text-gray-800">LHL Employee Management</h1>
            <div class="flex items-center space-x-4">
                <img src="https://placehold.co/80x50?text=LHL+Logo" alt="LHL Technologies company logo with blue and white colors" class="h-10">
            </div>
        </div>
           <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
            <!-- Employee Form -->
            <div class="bg-white rounded-lg shadow-lg p-6 no-print">
                <h2 class="text-xl font-semibold mb-4 text-gray-800">Employee Details</h2>
                <form id="employeeForm" class="space-y-4">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">First Name</label>
                            <input type="text" required id="empName" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                             <label class="block text-sm font-medium text-gray-700 mb-1">Emp Id</label>
                            <input type="text" required id="empName" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Last Name</label>
                      <input type="text" required id="emp id" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                            <label class="block text-sm font-medium text-gray-700 mb-1">Date Of Joining</label>
                      <input type="text" required id="emp id" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                   
</div>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Employee Photo</label>
                            <div class="flex items-center space-x-4">
                                <img id="photoPreview" src="https://placehold.co/100x100?text=Photo" alt="Employee photo placeholder" class="rounded-full h-16 w-16 object-cover border-2 border-gray-300">
                                <input type="file" id="empPhoto" accept="image/*" class="hidden">
                                <button type="button" onclick="document.getElementById('empPhoto').click()" class="px-3 py-1 bg-blue-500 text-white rounded-md hover:bg-blue-600">Upload</button>
                            </div>
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Department</label>
                            <select id="empDept" required class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option value="">Select Department</option>
                                <option value="IT">IT</option>
                                <option value="HR">HR</option>
                                <option value="Finance">Finance</option>
                                <option value="Marketing">Marketing</option>
                                <option value="Operations">Operations</option>
                                <option value="Sales">Sales</option>
                                <option value="R&D">R&D</option>
                            </select>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Designation</label>
                            <input type="text" required id="empDesignation" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Blood Group</label>
                            <select id="empBloodGroup" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option value="">Select Blood Group</option>
                                <option value="A+">A+</option>
                                <option value="A-">A-</option>
                                <option value="B+">B+</option>
                                <option value="B-">B-</option>
                                <option value="AB+">AB+</option>
                                <option value="AB-">AB-</option>
                                <option value="O+">O+</option>
                                <option value="O-">O-</option>
                            </select>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Mobile Number</label>
                            <input type="tel" required id="empMobile" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Email ID</label>
                            <input type="email" required id="empEmail" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Communication Address</label>
                        <textarea id="empCommAddress" rows="2" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Permanent Address</label>
                        <textarea id="empPermAddress" rows="2" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
                    </div>

                    <div>
                    <div class="pt-4">
                        <button type="submit" class="px-6 py-2 bg-blue-600 text-white rounded-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">Save Employee</button>
                        <button type="button" id="resetForm" class="px-6 py-2 ml-3 bg-gray-200 text-gray-800 rounded-md hover:bg-gray-300 focus:outline-none focus:ring-2 focus:ring-gray-500 focus:ring-offset-2">Reset</button>
                    </div>
                </form>
            </div>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Employee ID Card Generator</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f7fa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .id-card-container {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .id-card {
            width: 350px;
            height: 500px;
            perspective: 1000px;
            margin-bottom: 20px;
        }

        .id-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
            transition: transform 0.8s;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .id-card:hover .id-card-inner {
            transform: rotateY(180deg);
        }

        .id-card-front, .id-card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 15px;
            overflow: hidden;
        }

        .id-card-front {
            background: linear-gradient(135deg, #4a89dc, #5d9cec);
            color: white;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .id-card-back {
            background-color: white;
            transform: rotateY(180deg);
            display: flex;
            flex-direction: column;
            padding: 20px;
            color: #333;
        }

        .company-header {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 15px;
            width: 100%;
        }

        .company-logo {
            width: 50px;
            height: 50px;
            margin-right: 10px;
            background-color: white;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #4a89dc;
            font-size: 20px;
        }

        .company-name {
            font-size: 22px;
            font-weight: 700;
        }

        .employee-photo {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid white;
            margin: 15px 0;
            overflow: hidden;
            background-color: #e0e0e0;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .employee-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .employee-name {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .employee-id {
            font-size: 16px;
            margin-bottom: 15px;
            background-color: rgba(255, 255, 255, 0.2);
            padding: 5px 15px;
            border-radius: 20px;
        }

        .employee-details {
            width: 100%;
            margin-top: 15px;
        }

        .detail-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding-bottom: 8px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }

        .detail-label {
            font-weight: 600;
            font-size: 14px;
            text-align: left;
            flex: 1;
        }

        .detail-value {
            font-size: 14px;
            text-align: right;
            flex: 1;
        }

        .back-header {
            font-size: 18px;
            font-weight: 700;
            color: #4a89dc;
            margin-bottom: 20px;
            text-align: center;
            padding-bottom: 10px;
            border-bottom: 2px solid #4a89dc;
        }

        .company-address {
            font-size: 14px;
            line-height: 1.6;
            margin-bottom: 20px;
            text-align: center;
        }

        .emergency-contact {
            background-color: #f5f7fa;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .emergency-title {
            font-weight: 700;
            margin-bottom: 10px;
            color: #4a89dc;
            text-align: center;
        }

        .emergency-details {
            font-size: 14px;
            line-height: 1.6;
            text-align: center;
        }
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Signature Creator</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            margin: 0;
            padding: 20px;
            background-color: #f5f7fa;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .header h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #7f8c8d;
        }
        
        .signature-container {
            width: 100%;
            max-width: 800px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 20px;
        }
        
        .canvas-wrapper {
            position: relative;
            width: 100%;
            height: 200px;
            border: 1px dashed #ccc;
            margin-bottom: 20px;
        }
        
        #signatureCanvas {
            width: 100%;
            height: 100%;
            background-color: #fff;
            cursor: crosshair;
        }
        
        .tools {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .color-picker, .pen-size {
            display: flex;
            align-items: center;
        }
        
        .color-picker label, .pen-size label {
            margin-right: 10px;
            color: #2c3e50;
            font-weight: 500;
        }
        
        #penColor {
            width: 40px;
            height: 40px;
            border: none;
            cursor: pointer;
        }
        
        #penSize {
            width: 80px;
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .clear-btn {
            background-color: #e74c3c;
            color: white;
        }
        
        .clear-btn:hover {
            background-color: #c0392b;
        }
        
        .save-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .save-btn:hover {
            background-color: #27ae60;
        }
        
        .upload-btn {
            background-color: #3498db;
            color: white;
        }
        
        .upload-btn:hover {
            background-color: #2980b9;
        }
        
        .instructions {
            margin-top: 30px;
            background-color: #e8f4f8;
            padding: 15px;
            border-radius: 8px;
            color: #2c3e50;
            width: 100%;
            max-width: 800px;
        }
        
        .instructions h3 {
            margin-top: 0;
            color: #3498db;
        }
        
        .file-input {
            display: none;
        }
        
        .placeholder-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #bdc3c7;
            pointer-events: none;
        }
        
        @media (max-width: 600px) {
            .tools {
                flex-direction: column;
            }
            
            .action-buttons {
                flex-direction: column;
            }
            
            button {
                width: 100%;
            }
        }
    </style>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Signature Creator</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            margin: 0;
            padding: 20px;
            background-color: #f5f7fa;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .header h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #7f8c8d;
        }
        
        .signature-container {
            width: 100%;
            max-width: 800px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 20px;
        }
        
        .canvas-wrapper {
            position: relative;
            width: 100%;
            height: 200px;
            border: 1px dashed #ccc;
            margin-bottom: 20px;
        }
        
        #signatureCanvas {
            width: 100%;
            height: 100%;
            background-color: #fff;
            cursor: crosshair;
        }
        
        .tools {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .color-picker, .pen-size {
            display: flex;
            align-items: center;
        }
        
        .color-picker label, .pen-size label {
            margin-right: 10px;
            color: #2c3e50;
            font-weight: 500;
        }
        
        #penColor {
            width: 40px;
            height: 40px;
            border: none;
            cursor: pointer;
        }
        
        #penSize {
            width: 80px;
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .clear-btn {
            background-color: #e74c3c;
            color: white;
        }
        
        .clear-btn:hover {
            background-color: #c0392b;
        }
        
        .save-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .save-btn:hover {
            background-color: #27ae60;
        }
        
        .upload-btn {
            background-color: #3498db;
            color: white;
        }
        
        .upload-btn:hover {
            background-color: #2980b9;
        }
        
        .instructions {
            margin-top: 30px;
            background-color: #e8f4f8;
            padding: 15px;
            border-radius: 8px;
            color: #2c3e50;
            width: 100%;
            max-width: 800px;
        }
        
        .instructions h3 {
            margin-top: 0;
            color: #3498db;
        }
        
        .file-input {
            display: none;
        }
        
        .placeholder-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #bdc3c7;
            pointer-events: none;
        }
        
        @media (max-width: 600px) {
            .tools {
                flex-direction: column;
            }
            
            .action-buttons {
                flex-direction: column;
            }
            
            button {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        </div>
    <div class="signature-container">
        <div class="canvas-wrapper">
            <canvas id="signatureCanvas"></canvas>
            <div class="placeholder-text">Draw your signature here</div>
        </div>
        
        <div class="tools">
            <div class="color-picker">
                <label for="penColor">Pen Color:</label>
                <input type="color" id="penColor" value="#000000">
            </div>
            
            <div class="pen-size">
                <label for="penSize">Pen Size:</label>
                <input type="range" id="penSize" min="1" max="10" value="2">
            </div>
        </div>
        
        <div class="action-buttons">
            <button class="clear-btn" id="clearBtn">Clear Signature</button>
            <button class="save-btn" id="saveBtn">Save Signature</button>
            <button class="upload-btn" id="uploadBtn">Upload Signature</button>
            <input type="file" id="fileInput" class="file-input" accept="image/*">
        </div>
    </div>
   </div>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const canvas = document.getElementById('signatureCanvas');
            const ctx = canvas.getContext('2d');
            const placeholderText = document.querySelector('.placeholder-text');
            const penColor = document.getElementById('penColor');
            const penSize = document.getElementById('penSize');
            const clearBtn = document.getElementById('clearBtn');
            const saveBtn = document.getElementById('saveBtn');
            const uploadBtn = document.getElementById('uploadBtn');
            const fileInput = document.getElementById('fileInput');
            
            let isDrawing = false;
            let lastX = 0;
            let lastY = 0;
            
            // Set canvas size
            function resizeCanvas() {
                const rect = canvas.parentElement.getBoundingClientRect();
                canvas.width = rect.width;
                canvas.height = rect.height;
                canvas.style.width = rect.width + 'px';
                canvas.style.height = rect.height + 'px';
            }
            
            // Initial resize
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // Drawing functions
            function startDrawing(e) {
                isDrawing = true;
                [lastX, lastY] = getCoordinates(e);
                placeholderText.style.display = 'none';
            }
            
            function draw(e) {
                if (!isDrawing) return;
                
                ctx.strokeStyle = penColor.value;
                ctx.lineWidth = penSize.value;
                ctx.lineJoin = 'round';
                ctx.lineCap = 'round';
                
                const [x, y] = getCoordinates(e);
                
                ctx.beginPath();
                ctx.moveTo(lastX, lastY);
                ctx.lineTo(x, y);
                ctx.stroke();
                
                [lastX, lastY] = [x, y];
            }
            
            function stopDrawing() {
                isDrawing = false;
            }
            
            function getCoordinates(e) {
                let x, y;
                if (e.type.includes('touch')) {
                    x = e.touches[0].clientX - canvas.getBoundingClientRect().left;
                    y = e.touches[0].clientY - canvas.getBoundingClientRect().top;
                } else {
                    x = e.offsetX;
                    y = e.offsetY;
                }
                return [x, y];
            }
            
            // Event listeners for drawing
            canvas.addEventListener('mousedown', startDrawing);
            canvas.addEventListener('mousemove', draw);
            canvas.addEventListener('mouseup', stopDrawing);
            canvas.addEventListener('mouseout', stopDrawing);
            
            // Touch support
            canvas.addEventListener('touchstart', function(e) {
                e.preventDefault();
                startDrawing(e);
            });
            
            canvas.addEventListener('touchmove', function(e) {
                e.preventDefault();
                draw(e);
            });
            
            canvas.addEventListener('touchend', stopDrawing);
            
            // Clear canvas
            clearBtn.addEventListener('click', function() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                placeholderText.style.display = 'block';
            });
            
            // Save signature
            saveBtn.addEventListener('click', function() {
                if (isCanvasEmpty(canvas)) {
                    alert('Please create a signature first');
                    return;
                }
                
                const link = document.createElement('a');
                link.download = 'signature.png';
                link.href = canvas.toDataURL('image/png');
                link.click();
            });
            
            // Upload signature
            uploadBtn.addEventListener('click', function() {
                fileInput.click();
            });
            
            fileInput.addEventListener('change', function(e) {
                if (e.target.files && e.target.files[0]) {
                    const reader = new FileReader();
                    
                    reader.onload = function(event) {
                        const img = new Image();
                        img.onload = function() {
                            // Clear canvas
                            ctx.clearRect(0, 0, canvas.width, canvas.height);
                            placeholderText.style.display = 'none';
                            
                            // Calculate dimensions to fit the canvas while maintaining aspect ratio
                            const scale = Math.min(
                                canvas.width / img.width,
                                canvas.height / img.height
                            );
                            const width = img.width * scale;
                            const height = img.height * scale;
                            const x = (canvas.width - width) / 2;
                            const y = (canvas.height - height) / 2;
                            
                            // Draw the image
                            ctx.drawImage(img, x, y, width, height);
                        };
                        img.src = event.target.result;
                    };
                    
                    reader.readAsDataURL(e.target.files[0]);
                }
            });
            
            // Check if canvas is empty
            function isCanvasEmpty(canvas) {
                const blank = document.createElement('canvas');
                blank.width = canvas.width;
                blank.height = canvas.height;
                return canvas.toDataURL() === blank.toDataURL();
            }
        });
    </script>
</body>
</html>
    </style>
</head>
<body>
    <div class="id-card-container">
        <div class="id-card">
            <div class="id-card-inner">
                <div class="id-card-front">
                    <div class="company-header">
                        <div class="company-logo">LHL</div>
                        <div class="company-name">Lighthouse Labs</div>
                    </div>
                    
                    <div class="employee-photo">
                        <img src="https://placehold.co/400x400" alt="Professional headshot of employee with neutral background" />
                    </div>
                    
                    <div class="employee-name">John Doe</div>
                    <div class="employee-id">LHL00456</div>
                    
                    <div class="employee-details">
                        <div class="detail-row">
                            <div class="detail-label">Department:</div>
                            <div class="detail-value">Information Technology</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Designation:</div>
                            <div class="detail-value">Senior Developer</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Mobile:</div>
                            <div class="detail-value">+91 9876543210</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Date of Joining:</div>
                            <div class="detail-value">15 Jan 2020</div>
                        </div>
                        <div class="detail-row">
                            <div class="detail-label">Blood Group:</div>
                            <div class="detail-value">B+</div>
                        </div>
                    </div>
                </div>
                
                <div class="id-card-back">
                    <div class="back-header">Lighthouse Labs</div>
                    
                    <div class="company-address">
                        123 Tech Park, Sector 12<br>
                        Cyber City, Gurgaon<br>
                        Haryana - 122001, India<br>
                        www.lighthouselabs.com
                    </div>
                    
                    <div class="emergency-contact">
                        <div class="emergency-title">In Case of Emergency</div>
                        <div class="emergency-details">
                            Contact HR Department<br>
                            Phone: +91 124 4567890<br>
                            Email: hr@lighthouselabs.com
                        </div>
                    </div>
                    
                    <div class="signature-area">
                        <div class="signature-line"></div>
                        <div class="signature-label">Authorized Signature</div>
                    </div>
                    
                    <div class="validity">Valid until: 31 Dec 2024</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const departments = [
            "Information Technology",
            "Human Resources",
            "Finance",
            "Marketing",
            "Operations",
            "Sales",
            "Customer Support",
            "Research & Development"
        ];

        const designations = {
            "Information Technology": ["Junior Developer", "Developer", "Senior Developer", "Tech Lead", "Manager"],
            "Human Resources": ["HR Associate", "HR Manager", "HR Director"],
            "Finance": ["Accountant", "Financial Analyst", "Finance Manager"],
            "Marketing": ["Marketing Associate", "Marketing Manager"],
            "Operations": ["Operations Executive", "Operations Manager"],
            "Sales": ["Sales Executive", "Sales Manager"],
            "Customer Support": ["Support Executive", "Support Manager"],
            "Research & Development": ["Research Associate", "Research Scientist"]
        };

        const bloodGroups = ["A+", "A-", "B+", "B-", "AB+", "AB-", "O+", "O-"];

        function generateEmployeeCard() {
            // Generate random employee details
            const firstName = getRandomName();
            const lastName = getRandomName();
            const empName = `${firstName} ${lastName}`;
            
            // Generate employee ID in format LHLXXXXX (XXXXX from 00001 to 10000)
            const empIdNum = Math.floor(Math.random() * 10000) + 1;
            const empId = `LHL${empIdNum.toString().padStart(5, '0')}`;
            
            const department = departments[Math.floor(Math.random() * departments.length)];
            const designation = designations[department][Math.floor(Math.random() * designations[department].length)];
            
            // Generate random phone number
            const mobileNumber = `+91 ${Math.floor(1000000000 + Math.random() * 9000000000).toString().substring(1, 11)}`;
            
            // Generate random date of joining (between 2015 and 2023)
            const joinYear = Math.floor(Math.random() * 9) + 2015;
            const joinMonth = Math.floor(Math.random() * 12);
            const joinDay = Math.floor(Math.random() * 28) + 1;
            const joinDate = new Date(joinYear, joinMonth, joinDay);
            const options = { day: '2-digit', month: 'short', year: 'numeric' };
            const formattedDate = joinDate.toLocaleDateString('en-US', options);
            
            const bloodGroup = bloodGroups[Math.floor(Math.random() * bloodGroups.length)];
            
            // Generate random photo placeholder with different dimensions
            const photoWidth = Math.floor(Math.random() * 200) + 400;
            const photoHeight = photoWidth; // Keep it square
            
            // Update the DOM elements
            document.querySelector('.employee-name').textContent = empName;
            document.querySelector('.employee-id').textContent = empId;
            document.querySelector('.employee-photo img').src = `https://placehold.co/${photoWidth}x${photoHeight}`;
            document.querySelector('.employee-photo img').alt = `Professional headshot of ${empName}`;
            
            const detailRows = document.querySelectorAll('.detail-row');
            detailRows[0].querySelector('.detail-value').textContent = department;
            detailRows[1].querySelector('.detail-value').textContent = designation;
            detailRows[2].querySelector('.detail-value').textContent = mobileNumber;
            detailRows[3].querySelector('.detail-value').textContent = formattedDate;
            detailRows[4].querySelector('.detail-value').textContent = bloodGroup;
            
            // Generate random validity date
            const validityYear = joinYear + Math.floor(Math.random() * 5) + 1;
            document.querySelector('.validity').textContent = `Valid until: 31 Dec ${validityYear}`;
        }

        function getRandomName() {
            const names = [
                "Aarav", "Aditi", "Arjun", "Avni", "Dev", "Dhruv", "Diya", "Ishaan",
                "Kavya", "Kiara", "Mohit", "Neha", "Parth", "Prisha", "Reyansh", "Riya",
                "Shaurya", "Siya", "Soham", "Tanvi", "Ved", "Yash", "Zara",
                "John", "Michael", "David", "Sarah", "Jennifer", "Robert", "Emily", "Daniel",
                "Lisa", "William", "Jessica", "Christopher", "Ashley", "Matthew", "Amanda",
                "James", "Elizabeth", "Andrew", "Nicole", "Ryan", "Stephanie"
            ];
            return names[Math.floor(Math.random() * names.length)];
        }

        // Generate an initial card when page loads
        window.onload = function() {
            generateEmployeeCard();
        };
    </script>
</body>
</html>
 <!-- Employee List -->
            <div class="bg-white rounded-lg shadow-md p-6 animate-in">
                <div class="flex justify-between items-center mb-4">
                    <h2 class="text-xl font-semibold text-gray-800">Employee List</h2>
                    <div class="relative">
                        <input type="text" id="searchInput" placeholder="Search employees..." class="px-4 py-2 border border-gray-1000 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-1000">
                    </div>
                </div>

                <div id="employeeList" class="space-y-4">
                    <!-- Employee cards will be added here dynamically -->
                    <div class="text-center text-gray-500 py-8">
                        <p>No employees added yet. Add your first employee above!</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const employeeForm = document.getElementById('employeeForm');
            const employeeList = document.getElementById('employeeList');
            const searchInput = document.getElementById('searchInput');
            let employees = JSON.parse(localStorage.getItem('employees')) || [];

            // Render all employees initially
            renderEmployeeList(employees);

            // Add new employee
            employeeForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                const employee = {
                    id: Date.now(),
                    name: document.getElementById('name').value,
                    email: document.getElementById('email').value,
                    position: document.getElementById('position').value,
                    department: document.getElementById('department').value,
                    dateAdded: new Date().toLocaleDateString()
                };

                employees.push(employee);
                localStorage.setItem('employees', JSON.stringify(employees));
                
                renderEmployeeList(employees);
                employeeForm.reset();
                
                // Show success message
                alert('Employee added successfully!');
            });

            // Search functionality
            searchInput.addEventListener('input', function() {
                const searchTerm = this.value.toLowerCase();
                const filteredEmployees = employees.filter(employee => {
                    return (
                        employee.name.toLowerCase().includes(searchTerm) ||
                        employee.email.toLowerCase().includes(searchTerm) ||
                        employee.position.toLowerCase().includes(searchTerm) ||
                        employee.department.toLowerCase().includes(searchTerm)
                    );
                });
                renderEmployeeList(filteredEmployees);
            });

            // Render employee list
            function renderEmployeeList(employeeArray) {
                if (employeeArray.length === 0) {
                    employeeList.innerHTML = `
                        <div class="text-center text-gray-500 py-8">
                            <p>No employees found.</p>
                        </div>
                    `;
                    return;
                }

                employeeList.innerHTML = '';
                
                employeeArray.forEach(employee => {
                    const employeeCard = document.createElement('div');
                    employeeCard.className = 'employee-card bg-white border border-gray-200 rounded-lg overflow-hidden shadow-sm cursor-pointer';
                    employeeCard.innerHTML = `
                        <div class="p-4">
                            <div class="flex items-start">
                                <div class="flex-shrink-0">
                                    <img src="https://placehold.co/80x80/${getDepartmentColor(employee.department)}/FFFFFF?text=${employee.name.charAt(0)}" 
                                         alt="Profile picture placeholder for ${employee.name}" 
                                         class="rounded-full h-12 w-12 object-cover">
                                </div>
                                <div class="ml-4 flex-1">
                                    <div class="flex items-center justify-between">
                                        <h3 class="text-lg font-medium text-gray-900">${employee.name}</h3>
                                        <span class="px-2 py-1 text-xs font-medium rounded-full ${getDepartmentBadgeColor(employee.department)}">
                                            ${employee.department}
                                        </span>
                                    </div>
                                    <p class="text-sm text-gray-600">${employee.position}</p>
                                    <div class="mt-2 grid grid-cols-2 gap-1 text-sm text-gray-500">
                                        <div class="flex items-center">
                                            <svg class="h-4 w-4 mr-1 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                                            </svg>
                                            ${employee.email}
                                        </div>
                                        <div class="flex items-center">
                                            <svg class="h-4 w-4 mr-1 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
                                            </svg>
                                            Added: ${employee.dateAdded}
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    `;
                    employeeList.appendChild(employeeCard);
                });
            }

            // Helper functions for department colors
            function getDepartmentColor(department) {
                const colors = {
                    'IT': '4F46E5',
                    'HR': 'EC4899',
                    'Finance': '10B981',
                    'Marketing': 'F59E0B',
                    'Operations': '3B82F6'
                };
                return colors[department] || '6B7280';
            }

            function getDepartmentBadgeColor(department) {
                const colors = {
                    'IT': 'bg-indigo-100 text-indigo-800',
                    'HR': 'bg-pink-100 text-pink-800',
                    'Finance': 'bg-green-100 text-green-800',
                    'Marketing': 'bg-yellow-100 text-yellow-800',
                    'Operations': 'bg-blue-100 text-blue-800'
                };
                return colors[department] || 'bg-gray-100 text-gray-800';
            }
        });
    </script>
</body>
</html>
