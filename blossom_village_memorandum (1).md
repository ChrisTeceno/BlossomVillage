<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blossom Village - Offering Memorandum</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 0 30px rgba(0,0,0,0.3);
        }
        
        .header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 60px 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="1"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
            opacity: 0.3;
        }
        
        .header-content {
            position: relative;
            z-index: 1;
        }
        
        .property-title {
            font-size: 3em;
            font-weight: bold;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .property-subtitle {
            font-size: 1.2em;
            margin-bottom: 20px;
            opacity: 0.9;
        }
        
        .price-banner {
            background: rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            padding: 20px;
            border-radius: 15px;
            display: inline-block;
            margin-top: 20px;
        }
        
        .price {
            font-size: 2.5em;
            font-weight: bold;
            color: #ffd700;
        }
        
        .nav {
            background: #2c3e50;
            padding: 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
        }
        
        .nav li {
            margin: 0;
        }
        
        .nav a {
            display: block;
            padding: 15px 25px;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
        }
        
        .nav a:hover {
            background: #34495e;
            border-bottom: 3px solid #3498db;
        }
        
        .section {
            padding: 60px 40px;
            border-bottom: 1px solid #eee;
        }
        
        .section-title {
            font-size: 2.5em;
            color: #2c3e50;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background: linear-gradient(135deg, #3498db, #2ecc71);
            margin: 20px auto;
        }
        
        .highlight-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }
        
        .highlight-card {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border-left: 5px solid #3498db;
        }
        
        .highlight-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }
        
        .highlight-icon {
            font-size: 3em;
            margin-bottom: 15px;
            display: block;
        }
        
        .highlight-title {
            font-size: 1.4em;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 15px;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }
        
        .stat-box {
            background: white;
            padding: 30px;
            text-align: center;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border-top: 4px solid #3498db;
        }
        
        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            color: #2c3e50;
            display: block;
        }
        
        .stat-label {
            color: #7f8c8d;
            font-size: 0.9em;
            text-transform: uppercase;
            margin-top: 10px;
        }
        
        .image-placeholder {
            width: 100%;
            height: 400px;
            background: linear-gradient(135deg, #bdc3c7 0%, #95a5a6 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 15px;
            margin: 30px 0;
            color: white;
            font-size: 1.2em;
            text-align: center;
            box-shadow: inset 0 0 50px rgba(0,0,0,0.2);
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }
        
        .gallery-item {
            background: #f8f9fa;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .gallery-item:hover {
            transform: scale(1.03);
        }
        
        .gallery-placeholder {
            width: 100%;
            height: 250px;
            background: linear-gradient(135deg, #95a5a6 0%, #7f8c8d 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        .gallery-caption {
            padding: 20px;
            font-weight: bold;
            color: #2c3e50;
        }
        
        .floor-plan {
            background: white;
            border: 2px solid #3498db;
            border-radius: 15px;
            padding: 30px;
            margin: 30px 0;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .floor-plan-title {
            font-size: 1.5em;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .amenities-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .amenity-item {
            background: #ecf0f1;
            padding: 15px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            transition: background 0.3s ease;
        }
        
        .amenity-item:hover {
            background: #d5dbdb;
        }
        
        .amenity-icon {
            margin-right: 10px;
            font-size: 1.2em;
        }
        
        .cta-section {
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            color: white;
            padding: 60px 40px;
            text-align: center;
        }
        
        .cta-button {
            background: #e74c3c;
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 50px;
            font-size: 1.2em;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            margin: 20px 10px;
            box-shadow: 0 10px 25px rgba(231, 76, 60, 0.3);
        }
        
        .cta-button:hover {
            background: #c0392b;
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(231, 76, 60, 0.4);
        }
        
        .disclaimer {
            background: #34495e;
            color: #bdc3c7;
            padding: 40px;
            font-size: 0.9em;
            line-height: 1.8;
        }
        
        @media (max-width: 768px) {
            .property-title {
                font-size: 2em;
            }
            
            .section {
                padding: 40px 20px;
            }
            
            .nav ul {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="header-content">
                <h1 class="property-title">BLOSSOM VILLAGE</h1>
                <p class="property-subtitle">9509 Folsom Boulevard • Rancho Cordova, CA 95827</p>
                <p class="property-subtitle">Mixed-Use Development Opportunity</p>
                <div class="price-banner">
                    <div class="price">$2,200,000</div>
                </div>
            </div>
        </div>

        <!-- Navigation -->
        <nav class="nav">
            <ul>
                <li><a href="#overview">Overview</a></li>
                <li><a href="#highlights">Highlights</a></li>
                <li><a href="#visuals">Visuals</a></li>
                <li><a href="#market">Market</a></li>
                <li><a href="#development">Development</a></li>
            </ul>
        </nav>

        <!-- Property Overview -->
        <section id="overview" class="section">
            <h2 class="section-title">Investment Overview</h2>
            
            <div class="stats-container">
                <div class="stat-box">
                    <span class="stat-number">2.0</span>
                    <span class="stat-label">Total Acres</span>
                </div>
                <div class="stat-box">
                    <span class="stat-number">80</span>
                    <span class="stat-label">Max Units</span>
                </div>
                <div class="stat-box">
                    <span class="stat-number">33%</span>
                    <span class="stat-label">Operating Hotel</span>
                </div>
                <div class="stat-box">
                    <span class="stat-number">2</span>
                    <span class="stat-label">Story Development</span>
                </div>
            </div>

            <p style="font-size: 1.2em; text-align: center; margin: 40px 0; color: #555;">
                <strong>Blossom Village</strong> presents a unique mixed-use development opportunity on a strategically located 2-acre parcel along Folsom Boulevard in Rancho Cordova, California. This exceptional property features both immediate income generation and substantial future development potential, making it an ideal acquisition for investors seeking both cash flow and value creation opportunities.
            </p>
        </section>

        <!-- Investment Highlights -->
        <section id="highlights" class="section" style="background: #f8f9fa;">
            <h2 class="section-title">Investment Highlights</h2>
            
            <div class="highlight-grid">
                <div class="highlight-card">
                    <span class="highlight-icon">💰</span>
                    <h3 class="highlight-title">Immediate Cash Flow</h3>
                    <p>Operational hotel facility on half the property provides immediate income generation while development plans are finalized.</p>
                </div>
                
                <div class="highlight-card">
                    <span class="highlight-icon">🏗️</span>
                    <h3 class="highlight-title">Substantial Development Rights</h3>
                    <p>Zoning accommodates up to 80 extended-stay units across two stories, maximizing land utilization and revenue potential.</p>
                </div>
                
                <div class="highlight-card">
                    <span class="highlight-icon">🔄</span>
                    <h3 class="highlight-title">Flexible Development Options</h3>
                    <p>Existing hotel can remain operational during phased development or be demolished to maximize new construction potential.</p>
                </div>
                
                <div class="highlight-card">
                    <span class="highlight-icon">📍</span>
                    <h3 class="highlight-title">Prime Location Benefits</h3>
                    <p>Direct access to Folsom Boulevard, close proximity to churches, schools, businesses, and easy highway access for regional connectivity.</p>
                </div>
                
                <div class="highlight-card">
                    <span class="highlight-icon">📈</span>
                    <h3 class="highlight-title">Growing Market Demand</h3>
                    <p>Extended stay hotel market achieved $57.2 billion in 2024 with projected growth, driven by digital nomads and business travelers.</p>
                </div>
                
                <div class="highlight-card">
                    <span class="highlight-icon">🌟</span>
                    <h3 class="highlight-title">Sacramento Market Strength</h3>
                    <p>Sacramento's multifamily market shows record renter demand with 95.5% occupancy rate, indicating strong housing fundamentals.</p>
                </div>
            </div>
        </section>

        <!-- Property Visuals -->
        <section id="visuals" class="section">
            <h2 class="section-title">Property Visuals & Renderings</h2>
            
            <!-- Aerial/Location Images -->
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="AerialView.png" alt="Aerial view of Blossom Village property" style="width:100%; height:250px; object-fit:cover; border-radius:15px;" />
                    <div class="gallery-caption">Current Property Aerial View</div>
                </div>
                
                <div class="gallery-item">
                    <div class="gallery-placeholder">EXISTING HOTEL FACILITY</div>
                    <div class="gallery-caption">Operating Hotel (50% of Property)</div>
                </div>
                
                <div class="gallery-item">
                    <div class="gallery-placeholder">DEVELOPMENT AREA</div>
                    <div class="gallery-caption">Vacant Development Land (1 Acre)</div>
                </div>
            </div>

            <!-- Proposed Development Renderings -->
            <h3 style="font-size: 2em; text-align: center; margin: 50px 0 30px 0; color: #2c3e50;">Proposed Development Renderings</h3>
            
            <div class="gallery-grid">
                <div class="gallery-item">
                    <div class="gallery-placeholder">FRONT EXTERIOR RENDERING</div>
                    <div class="gallery-caption">Two-Story Extended Stay Hotel - Front View</div>
                </div>
                
                <div class="gallery-item">
                    <div class="gallery-placeholder">SIDE ELEVATION RENDERING</div>
                    <div class="gallery-caption">Building Side Elevation with Parking</div>
                </div>
                
                <div class="gallery-item">
                    <div class="gallery-placeholder">LANDSCAPING & ENTRANCE</div>
                    <div class="gallery-caption">Professional Landscaping & Main Entrance</div>
                </div>
            </div>

            <!-- Floor Plans -->
            <div class="floor-plan">
                <div class="floor-plan-title">Studio Extended Stay Unit Layout (400 sq ft)</div>
                <div class="image-placeholder">
                    DETAILED FLOOR PLAN<br>
                    • Dedicated Office Workspace<br>
                    • Full Kitchenette<br>
                    • Living/Sleeping Area<br>
                    • Walk-in Closet<br>
                    • Full Bathroom
                </div>
                
                <div class="amenities-list">
                    <div class="amenity-item">
                        <span class="amenity-icon">🛏️</span>
                        <span>Full-size bed with premium linens</span>
                    </div>
                    <div class="amenity-item">
                        <span class="amenity-icon">💻</span>
                        <span>Dedicated office workspace</span>
                    </div>
                    <div class="amenity-item">
                        <span class="amenity-icon">🍳</span>
                        <span>Full kitchenette with appliances</span>
                    </div>
                    <div class="amenity-item">
                        <span class="amenity-icon">📺</span>
                        <span>Flat-screen TV with streaming</span>
                    </div>
                    <div class="amenity-item">
                        <span class="amenity-icon">🌡️</span>
                        <span>Individual climate control</span>
                    </div>
                    <div class="amenity-item">
                        <span class="amenity-icon">📶</span>
                        <span>High-speed WiFi included</span>
                    </div>
                </div>
            </div>

            <!-- Community Areas -->
            <h3 style="font-size: 2em; text-align: center; margin: 50px 0 30px 0; color: #2c3e50;">Community Amenities</h3>
            
            <div class="gallery-grid">
                <div class="gallery-item">
                    <div class="gallery-placeholder">COMMUNITY LOUNGE RENDERING</div>
                    <div class="gallery-caption">1,200 sq ft Community Lounge & Co-Working Space</div>
                </div>
                
                <div class="gallery-item">
                    <div class="gallery-placeholder">FITNESS CENTER RENDERING</div>
                    <div class="gallery-caption">800 sq ft Professional Fitness Center</div>
                </div>
                
                <div class="gallery-item">
                    <div class="gallery-placeholder">BUSINESS CENTER RENDERING</div>
                    <div class="gallery-caption">Business Center with Coffee Bar</div>
                </div>
            </div>
        </section>

        <!-- Market Overview -->
        <section id="market" class="section" style="background: #f8f9fa;">
            <h2 class="section-title">Market Overview</h2>
            
            <div class="stats-container">
                <div class="stat-box">
                    <span class="stat-number">79,332</span>
                    <span class="stat-label">Population</span>
                </div>
                <div class="stat-box">
                    <span class="stat-number">$89,120</span>
                    <span class="stat-label">Median Income</span>
                </div>
                <div class="stat-box">
                    <span class="stat-number">95.5%</span>
                    <span class="stat-label">Occupancy Rate</span>
                </div>
                <div class="stat-box">
                    <span class="stat-number">$57.2B</span>
                    <span class="stat-label">Extended Stay Market</span>
                </div>
            </div>

            <div style="background: white; padding: 30px; border-radius: 15px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); margin: 40px 0;">
                <h3 style="color: #2c3e50; margin-bottom: 20px;">Rancho Cordova Market Fundamentals</h3>
                <ul style="list-style: none; padding: 0;">
                    <li style="padding: 10px 0; border-bottom: 1px solid #eee;">✓ Diverse community of over 85,000 residents and 65,000 workers</li>
                    <li style="padding: 10px 0; border-bottom: 1px solid #eee;">✓ 29th most diverse city in the United States</li>
                    <li style="padding: 10px 0; border-bottom: 1px solid #eee;">✓ Strong proximity to UC Davis Medical Center and corporate facilities</li>
                    <li style="padding: 10px 0; border-bottom: 1px solid #eee;">✓ Growing demand from business travelers and medical tourists</li>
                    <li style="padding: 10px 0;">✓ Sacramento metro area benefits from Bay Area business relocation</li>
                </ul>
            </div>
        </section>

        <!-- Development Opportunity -->
        <section id="development" class="section">
            <h2 class="section-title">Development Opportunity</h2>
            
            <div class="highlight-grid">
                <div class="highlight-card" style="border-left-color: #e74c3c;">
                    <span class="highlight-icon">🏢</span>
                    <h3 class="highlight-title">Current Configuration</h3>
                    <ul style="margin: 15px 0; padding-left: 20px;">
                        <li>Existing operational hotel facility</li>
                        <li>1 acre of vacant development land</li>
                        <li>Flexible integration or demolition options</li>
                    </ul>
                </div>
                
                <div class="highlight-card" style="border-left-color: #f39c12;">
                    <span class="highlight-icon">🏗️</span>
                    <h3 class="highlight-title">Development Potential</h3>
                    <ul style="margin: 15px 0; padding-left: 20px;">
                        <li>Maximum 80 extended-stay units</li>
                        <li>Two-story construction design</li>
                        <li>Modern amenities and workspace areas</li>
                        <li>Ample parking for guests and visitors</li>
                    </ul>
                </div>
                
                <div class="highlight-card" style="border-left-color: #27ae60;">
                    <span class="highlight-icon">🎯</span>
                    <h3 class="highlight-title">Target Market Segments</h3>
                    <ul style="margin: 15px 0; padding-left: 20px;">
                        <li>Business travelers on extended assignments</li>
                        <li>Medical patients and families</li>
                        <li>Temporary residents in transition</li>
                        <li>Government personnel and contractors</li>
                        <li>Corporate housing clients</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Call to Action -->
        <div class="cta-section">
            <h2 style="font-size: 2.5em; margin-bottom: 20px;">Ready to Move Forward?</h2>
            <p style="font-size: 1.2em; margin-bottom: 30px; max-width: 600px; margin-left: auto; margin-right: auto;">
                This exceptional mixed-use development opportunity represents a unique combination of immediate income generation and substantial future growth potential.
            </p>
            <a href="#" class="cta-button">Schedule Property Tour</a>
            <a href="#" class="cta-button" style="background: #27ae60;">Request Financial Analysis</a>
        </div>

        <!-- Disclaimer -->
        <div class="disclaimer">
            <p><strong>CONFIDENTIALITY & DISCLAIMER:</strong> This offering memorandum contains forward-looking statements and projections. Actual results may vary. All financial projections are estimates based on current market conditions and are subject to change. Prospective purchasers should conduct their own due diligence and financial analysis. The information contained herein has been obtained from sources believed to be reliable; however, no warranty or representation is made regarding the accuracy or completeness of the information provided.</p>
        </div>
    </div>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add parallax effect to header
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const header = document.querySelector('.header');
            header.style.transform = `translateY(${scrolled * 0.5}px)`;
        });
    </script>
</body>
</html>