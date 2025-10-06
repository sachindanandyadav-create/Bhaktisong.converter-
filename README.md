<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free QR Code Generator - Create custom QR codes for URLs, text, and more. Download high-quality QR codes instantly.">
    <meta name="keywords" content="QR code generator, QR code, free QR code, download QR code">
    <title>QR Code Generator Pro - Create Custom QR Codes Instantly</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #4361ee;
            --secondary: #3a0ca3;
            --accent: #7209b7;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4cc9f0;
            --gray: #6c757d;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            padding: 30px 0;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.1rem;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto;
        }

        .logo {
            font-size: 2rem;
            margin-bottom: 15px;
            color: white;
        }

        .main-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 30px;
        }

        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr;
            }
        }

        .card {
            background: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .card h2 {
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--light);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .card h2 i {
            color: var(--accent);
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--dark);
        }

        input, select, textarea {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #e1e5ee;
            border-radius: 10px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        input:focus, select:focus, textarea:focus {
            border-color: var(--primary);
            outline: none;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(to right, var(--primary), var(--accent));
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 10px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(67, 97, 238, 0.4);
        }

        .btn i {
            margin-right: 8px;
        }

        .btn-block {
            display: block;
            width: 100%;
        }

        .qr-container {
            text-align: center;
            padding: 20px;
        }

        .qr-code {
            width: 100%;
            max-width: 256px;
            height: auto;
            margin: 0 auto 20px;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .qr-placeholder {
            width: 100%;
            height: 256px;
            background: #f8f9fa;
            border: 2px dashed #dee2e6;
            border-radius: 10px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: var(--gray);
            margin-bottom: 20px;
        }

        .qr-placeholder i {
            font-size: 3rem;
            margin-bottom: 15px;
            color: #adb5bd;
        }

        .action-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .ads-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin: 30px 0;
        }

        @media (max-width: 768px) {
            .ads-container {
                grid-template-columns: 1fr;
            }
        }

        .ad-unit {
            background: white;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            min-height: 280px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px dashed #dee2e6;
        }

        .ad-label {
            font-size: 0.8rem;
            color: var(--gray);
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .ad-placeholder {
            width: 100%;
            height: 250px;
            background: #f8f9fa;
            border-radius: 5px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: var(--gray);
        }

        .ad-placeholder i {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }

        .feature {
            background: white;
            padding: 25px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .feature i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 15px;
        }

        .feature h3 {
            margin-bottom: 10px;
            color: var(--dark);
        }

        footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 50px;
            border-top: 1px solid #e1e5ee;
            color: var(--gray);
        }

        .color-options {
            display: flex;
            gap: 15px;
            margin-top: 10px;
        }

        .color-option {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid transparent;
            transition: transform 0.2s;
        }

        .color-option:hover {
            transform: scale(1.1);
        }

        .color-option.active {
            border-color: var(--dark);
        }

        .size-options {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .size-option {
            padding: 8px 15px;
            background: #f8f9fa;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .size-option.active {
            background: var(--primary);
            color: white;
        }

        .history-item {
            padding: 10px 15px;
            background: #f8f9fa;
            border-radius: 8px;
            margin-bottom: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .history-item:last-child {
            margin-bottom: 0;
        }

        .history-content {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .history-qr {
            width: 40px;
            height: 40px;
            background: #e9ecef;
            border-radius: 5px;
        }

        .history-actions {
            display: flex;
            gap: 10px;
        }

        .history-actions button {
            background: none;
            border: none;
            color: var(--gray);
            cursor: pointer;
            transition: color 0.2s;
        }

        .history-actions button:hover {
            color: var(--primary);
        }

        .toast {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--success);
            color: white;
            padding: 15px 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .toast.show {
            transform: translateY(0);
            opacity: 1;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <i class="fas fa-qrcode"></i>
            </div>
            <h1>QR Code Generator Pro</h1>
            <p>Create custom QR codes for URLs, text, contact info, and more. Free, fast, and easy to use!</p>
        </header>

        <div class="ads-container">
            <div class="ad-unit">
                <div class="ad-label">Advertisement</div>
                <div class="ad-placeholder">
                    <i class="fas fa-ad"></i>
                    <p>AdSense Ad Unit</p>
                    <p>320x250</p>
                </div>
            </div>
            <div class="ad-unit">
                <div class="ad-label">Advertisement</div>
                <div class="ad-placeholder">
                    <i class="fas fa-ad"></i>
                    <p>AdSense Ad Unit</p>
                    <p>320x250</p>
                </div>
            </div>
        </div>

        <div class="main-content">
            <div class="card">
                <h2><i class="fas fa-cog"></i> QR Code Settings</h2>
                
                <div class="form-group">
                    <label for="qr-content">Content for QR Code</label>
                    <textarea id="qr-content" rows="4" placeholder="Enter URL, text, or other content...">https://www.example.com</textarea>
                </div>
                
                <div class="form-group">
                    <label for="qr-type">QR Code Type</label>
                    <select id="qr-type">
                        <option value="url">URL</option>
                        <option value="text">Text</option>
                        <option value="email">Email</option>
                        <option value="wifi">Wi-Fi</option>
                        <option value="contact">Contact Info</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label>QR Code Color</label>
                    <div class="color-options">
                        <div class="color-option active" style="background-color: #000000;" data-color="#000000"></div>
                        <div class="color-option" style="background-color: #4361ee;" data-color="#4361ee"></div>
                        <div class="color-option" style="background-color: #e63946;" data-color="#e63946"></div>
                        <div class="color-option" style="background-color: #2a9d8f;" data-color="#2a9d8f"></div>
                        <div class="color-option" style="background-color: #7209b7;" data-color="#7209b7"></div>
                    </div>
                </div>
                
                <div class="form-group">
                    <label>QR Code Size</label>
                    <div class="size-options">
                        <div class="size-option active" data-size="200">Small</div>
                        <div class="size-option" data-size="256">Medium</div>
                        <div class="size-option" data-size="300">Large</div>
                    </div>
                </div>
                
                <button id="generate-btn" class="btn btn-block">
                    <i class="fas fa-bolt"></i> Generate QR Code
                </button>
            </div>
            
            <div class="card">
                <h2><i class="fas fa-qrcode"></i> Your QR Code</h2>
                
                <div class="qr-container">
                    <div class="qr-placeholder">
                        <i class="fas fa-qrcode"></i>
                        <p>Your QR code will appear here</p>
                    </div>
                    
                    <div class="action-buttons">
                        <button id="download-btn" class="btn" disabled>
                            <i class="fas fa-download"></i> Download
                        </button>
                        <button id="save-btn" class="btn" disabled>
                            <i class="fas fa-save"></i> Save to History
                        </button>
                        <button id="share-btn" class="btn" disabled>
                            <i class="fas fa-share-alt"></i> Share
                        </button>
                    </div>
                </div>
                
                <div class="form-group" style="margin-top: 20px;">
                    <h2><i class="fas fa-history"></i> Generation History</h2>
                    <div id="history-list">
                        <div class="history-item">
                            <div class="history-content">
                                <div class="history-qr"></div>
                                <div>
                                    <div class="history-title">Example QR Code</div>
                                    <div class="history-date">Just now</div>
                                </div>
                            </div>
                            <div class="history-actions">
                                <button title="Regenerate"><i class="fas fa-redo"></i></button>
                                <button title="Download"><i class="fas fa-download"></i></button>
                                <button title="Delete"><i class="fas fa-trash"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="features">
            <div class="feature">
                <i class="fas fa-bolt"></i>
                <h3>Fast Generation</h3>
                <p>Create QR codes in seconds with our optimized algorithm</p>
            </div>
            <div class="feature">
                <i class="fas fa-palette"></i>
                <h3>Customizable</h3>
                <p>Choose from different colors and sizes for your QR codes</p>
            </div>
            <div class="feature">
                <i class="fas fa-download"></i>
                <h3>Easy Download</h3>
                <p>Download your QR codes in high-quality PNG format</p>
            </div>
            <div class="feature">
                <i class="fas fa-history"></i>
                <h3>History Tracking</h3>
                <p>Keep track of all your generated QR codes</p>
            </div>
        </div>

        <div class="ads-container">
            <div class="ad-unit">
                <div class="ad-label">Advertisement</div>
                <div class="ad-placeholder">
                    <i class="fas fa-ad"></i>
                    <p>AdSense Ad Unit</p>
                    <p>728x90</p>
                </div>
            </div>
        </div>

        <footer>
            <p>QR Code Generator Pro &copy; 2023 | All Rights Reserved</p>
            <p>This tool is 100% free to use. No registration required.</p>
        </footer>
    </div>

    <div id="toast" class="toast">QR Code generated successfully!</div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // DOM Elements
            const generateBtn = document.getElementById('generate-btn');
            const downloadBtn = document.getElementById('download-btn');
            const saveBtn = document.getElementById('save-btn');
            const shareBtn = document.getElementById('share-btn');
            const qrContent = document.getElementById('qr-content');
            const qrType = document.getElementById('qr-type');
            const colorOptions = document.querySelectorAll('.color-option');
            const sizeOptions = document.querySelectorAll('.size-option');
            const qrPlaceholder = document.querySelector('.qr-placeholder');
            const historyList = document.getElementById('history-list');
            const toast = document.getElementById('toast');
            
            // Current settings
            let currentColor = '#000000';
            let currentSize = '256';
            let currentQRCode = null;
            
            // Color selection
            colorOptions.forEach(option => {
                option.addEventListener('click', function() {
                    colorOptions.forEach(opt => opt.classList.remove('active'));
                    this.classList.add('active');
                    currentColor = this.getAttribute('data-color');
                });
            });
            
            // Size selection
            sizeOptions.forEach(option => {
                option.addEventListener('click', function() {
                    sizeOptions.forEach(opt => opt.classList.remove('active'));
                    this.classList.add('active');
                    currentSize = this.getAttribute('data-size');
                });
            });
            
            // Generate QR Code
            generateBtn.addEventListener('click', function() {
                const content = qrContent.value.trim();
                if (!content) {
                    showToast('Please enter content for the QR code', 'error');
                    return;
                }
                
                // In a real implementation, this would call a QR code generation API
                // For this demo, we'll simulate generation
                simulateQRGeneration(content);
            });
            
            // Download QR Code
            downloadBtn.addEventListener('click', function() {
                if (!currentQRCode) return;
                
                // In a real implementation, this would download the actual QR code image
                showToast('QR Code downloaded successfully!');
                
                // Simulate download
                const link = document.createElement('a');
                link.download = `qrcode-${Date.now()}.png`;
                link.href = currentQRCode;
                link.click();
            });
            
            // Save to History
            saveBtn.addEventListener('click', function() {
                if (!currentQRCode) return;
                
                const content = qrContent.value.trim();
                const title = content.length > 30 ? content.substring(0, 30) + '...' : content;
                
                const historyItem = document.createElement('div');
                historyItem.className = 'history-item';
                historyItem.innerHTML = `
                    <div class="history-content">
                        <div class="history-qr" style="background: url('${currentQRCode}') center/cover;"></div>
                        <div>
                            <div class="history-title">${title}</div>
                            <div class="history-date">Just now</div>
                        </div>
                    </div>
                    <div class="history-actions">
                        <button title="Regenerate"><i class="fas fa-redo"></i></button>
                        <button title="Download"><i class="fas fa-download"></i></button>
                        <button title="Delete"><i class="fas fa-trash"></i></button>
                    </div>
                `;
                
                // Add event listeners to the new history item buttons
                const buttons = historyItem.querySelectorAll('.history-actions button');
                buttons[0].addEventListener('click', function() {
                    qrContent.value = content;
                    simulateQRGeneration(content);
                });
                
                buttons[1].addEventListener('click', function() {
                    const link = document.createElement('a');
                    link.download = `qrcode-${Date.now()}.png`;
                    link.href = currentQRCode;
                    link.click();
                });
                
                buttons[2].addEventListener('click', function() {
                    historyItem.remove();
                });
                
                historyList.prepend(historyItem);
                showToast('QR Code saved to history!');
            });
            
            // Share QR Code
            shareBtn.addEventListener('click', function() {
                if (!currentQRCode) return;
                
                if (navigator.share) {
                    navigator.share({
                        title: 'My QR Code',
                        text: 'Check out this QR code I generated!',
                        url: currentQRCode,
                    })
                    .then(() => showToast('QR Code shared successfully!'))
                    .catch(error => console.log('Error sharing:', error));
                } else {
                    showToast('Sharing not supported on this browser');
                }
            });
            
            // QR Type change
            qrType.addEventListener('change', function() {
                const type = this.value;
                let placeholder = 'Enter URL, text, or other content...';
                
                switch(type) {
                    case 'url':
                        placeholder = 'https://www.example.com';
                        break;
                    case 'text':
                        placeholder = 'Enter any text here...';
                        break;
                    case 'email':
                        placeholder = 'example@email.com';
                        break;
                    case 'wifi':
                        placeholder = 'WIFI:S:MyNetwork;T:WPA;P:MyPassword;;';
                        break;
                    case 'contact':
                        placeholder = 'BEGIN:VCARD\nVERSION:3.0\nFN:John Doe\nTEL:1234567890\nEMAIL:john@example.com\nEND:VCARD';
                        break;
                }
                
                qrContent.placeholder = placeholder;
                
                if (type === 'url' && qrContent.value === '') {
                    qrContent.value = 'https://www.example.com';
                }
            });
            
            // Simulate QR Code Generation
            function simulateQRGeneration(content) {
                // Show loading state
                generateBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Generating...';
                generateBtn.disabled = true;
                
                // In a real implementation, this would be an API call to generate the QR code
                // For this demo, we'll use a placeholder and simulate API delay
                setTimeout(() => {
                    // Create a canvas to simulate QR code generation
                    const canvas = document.createElement('canvas');
                    canvas.width = currentSize;
                    canvas.height = currentSize;
                    const ctx = canvas.getContext('2d');
                    
                    // Create a simple pattern that looks like a QR code
                    ctx.fillStyle = '#ffffff';
                    ctx.fillRect(0, 0, currentSize, currentSize);
                    
                    ctx.fillStyle = currentColor;
                    const blockSize = currentSize / 25;
                    
                    for (let i = 0; i < 25; i++) {
                        for (let j = 0; j < 25; j++) {
                            if (Math.random() > 0.5) {
                                ctx.fillRect(i * blockSize, j * blockSize, blockSize, blockSize);
                            }
                        }
                    }
                    
                    // Add positioning markers (like real QR codes have)
                    ctx.fillStyle = currentColor;
                    ctx.fillRect(0, 0, blockSize * 7, blockSize * 7);
                    ctx.fillRect(currentSize - blockSize * 7, 0, blockSize * 7, blockSize * 7);
                    ctx.fillRect(0, currentSize - blockSize * 7, blockSize * 7, blockSize * 7);
                    
                    ctx.fillStyle = '#ffffff';
                    ctx.fillRect(blockSize, blockSize, blockSize * 5, blockSize * 5);
                    ctx.fillRect(currentSize - blockSize * 6, blockSize, blockSize * 5, blockSize * 5);
                    ctx.fillRect(blockSize, currentSize - blockSize * 6, blockSize * 5, blockSize * 5);
                    
                    // Convert to data URL
                    currentQRCode = canvas.toDataURL('image/png');
                    
                    // Update the QR code display
                    qrPlaceholder.innerHTML = `<img src="${currentQRCode}" alt="Generated QR Code" class="qr-code">`;
                    
                    // Enable buttons
                    downloadBtn.disabled = false;
                    saveBtn.disabled = false;
                    shareBtn.disabled = false;
                    
                    // Reset generate button
                    generateBtn.innerHTML = '<i class="fas fa-bolt"></i> Generate QR Code';
                    generateBtn.disabled = false;
                    
                    showToast('QR Code generated successfully!');
                }, 1000);
            }
            
            // Show toast message
            function showToast(message, type = 'success') {
                toast.textContent = message;
                toast.className = 'toast';
                
                if (type === 'error') {
                    toast.style.background = '#e63946';
                } else {
                    toast.style.background = '#4cc9f0';
                }
                
                toast.classList.add('show');
                
                setTimeout(() => {
                    toast.classList.remove('show');
                }, 3000);
            }
            
            // Initialize with example QR code
            simulateQRGeneration('https://www.example.com');
        });
    </script>
</body>
</html>
