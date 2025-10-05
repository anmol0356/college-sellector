<MADE BY ANMOL>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kanpur College Finder - Find Your Perfect College</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .watermark {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.95);
            padding: 12px 20px;
            border-radius: 25px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            cursor: pointer;
            transition: all 0.3s ease;
            z-index: 1000;
            font-weight: 600;
            color: #667eea;
        }

        .watermark:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.3);
            background: #667eea;
            color: white;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        .header p {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .form-section {
            padding: 40px;
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #333;
            font-size: 1.1em;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 1em;
            transition: all 0.3s ease;
            resize: vertical;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }

        .submit-btn {
            width: 100%;
            padding: 18px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 1.2em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 20px;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
        }

        .compare-btn {
            width: 100%;
            padding: 12px;
            background: linear-gradient(135deg, #28a745 0%, #20c997 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 20px;
        }

        .compare-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(40, 167, 69, 0.3);
        }

        .results {
            padding: 40px;
            display: none;
        }

        .best-selects {
            background: linear-gradient(135deg, #4caf50 0%, #81c784 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 30px;
            text-align: center;
        }

        .best-selects h3 {
            font-size: 1.8em;
            margin-bottom: 15px;
        }

        .best-selects ul {
            list-style: none;
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        }

        .best-selects li {
            background: rgba(255,255,255,0.2);
            padding: 10px 20px;
            border-radius: 10px;
            margin: 5px;
        }

        .college-card {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 25px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
        }

        .college-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .college-checkbox {
            position: absolute;
            top: 15px;
            right: 15px;
        }

        .college-name {
            font-size: 1.8em;
            color: #667eea;
            margin-bottom: 15px;
            font-weight: 700;
        }

        .recommended-badge {
            display: inline-block;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9em;
            margin-bottom: 15px;
            font-weight: 600;
        }

        .college-info {
            margin: 20px 0;
        }

        .info-item {
            margin-bottom: 12px;
            line-height: 1.6;
        }

        .info-label {
            font-weight: 600;
            color: #333;
        }

        .yearly-programs-section {
            background: #e3f2fd;
            padding: 20px;
            border-radius: 10px;
            margin: 15px 0;
        }

        .courses-section {
            background: white;
            padding: 20px;
            border-radius: 10px;
            margin: 15px 0;
        }

        .course-tag {
            display: inline-block;
            background: #667eea;
            color: white;
            padding: 6px 12px;
            border-radius: 15px;
            margin: 5px;
            font-size: 0.9em;
        }

        .reviews-section {
            background: #fff3cd;
            padding: 20px;
            border-radius: 10px;
            margin: 15px 0;
        }

        .review {
            margin-bottom: 15px;
            padding: 15px;
            background: white;
            border-radius: 8px;
            border-left: 4px solid #667eea;
        }

        .review-author {
            font-weight: 600;
            color: #667eea;
            margin-bottom: 5px;
        }

        .star-rating {
            color: #ffc107;
            margin-bottom: 8px;
        }

        .highlights {
            background: #e8f5e9;
            padding: 20px;
            border-radius: 10px;
            margin: 15px 0;
        }

        .highlight-item {
            padding: 8px 0;
            display: flex;
            align-items: center;
        }

        .highlight-item:before {
            content: "✓";
            color: #4caf50;
            font-weight: bold;
            margin-right: 10px;
            font-size: 1.2em;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 2000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.4);
        }

        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 20px;
            border: none;
            border-radius: 10px;
            width: 90%;
            max-width: 1200px;
            max-height: 80vh;
            overflow-y: auto;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover {
            color: black;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }

        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }

        th {
            background-color: #667eea;
            color: white;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 1.8em;
            }
            
            .form-section {
                padding: 20px;
            }

            .best-selects ul {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="watermark" onclick="window.open('https://www.instagram.com/rajput_anmolsingh3', '_blank')">
        ANMOL SINGH / IG: rajput_anmolsingh3
    </div>

    <div class="container">
        <div class="header">
            <h1>🎓 Kanpur College Finder</h1>
            <p>Find Your Perfect College & Course Match</p>
        </div>

        <div class="form-section">
            <form id="collegeForm">
                <div class="form-group">
                    <label for="studentName">Your Name</label>
                    <input type="text" id="studentName" required placeholder="Enter your full name">
                </div>

                <div class="form-group">
                    <label for="percentage">Class 12th Percentage</label>
                    <input type="number" id="percentage" min="0" max="100" step="0.01" required placeholder="Enter your percentage (e.g., 85.5)">
                </div>

                <div class="form-group">
                    <label for="interest">Field of Interest</label>
                    <select id="interest" required>
                        <option value="">Select your interest</option>
                        <option value="Engineering">Engineering</option>
                        <option value="Medical">Medical</option>
                        <option value="Management">Management (MBA/BBA)</option>
                        <option value="Commerce">Commerce (B.Com/CA)</option>
                        <option value="Arts">Arts & Humanities</option>
                        <option value="Science">Pure Science</option>
                        <option value="Computer">Computer Applications (BCA/MCA)</option>
                        <option value="Law">Law</option>
                        <option value="Pharmacy">Pharmacy</option>
                        <option value="Architecture">Architecture</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="specificInterest">Specific Interests (e.g., experiments, college programs, sports, research)</label>
                    <textarea id="specificInterest" rows="3" placeholder="Describe what you're interested in, like lab experiments, annual fests, internships, etc."></textarea>
                </div>

                <button type="submit" class="submit-btn">Find My Perfect College 🚀</button>
            </form>
        </div>

        <div class="results" id="results"></div>
    </div>

    <!-- Comparison Modal -->
    <div id="compareModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>College Comparison</h2>
            <div id="comparisonTable"></div>
        </div>
    </div>

    <script>
        const colleges = [
            {
                name: "Flora Institute of Technology",
                minPercentage: 51,
                interests: ["Engineering"],
                specificKeywords: ["experiments", "labs", "workshops"],
                courses: ["B.Tech", "Diploma in Engineering"],
                yearlyPrograms: ["Freshers Party", "Tech Fest", "Annual Sports Day"],
                highlights: [
                    "Budget-friendly engineering education",
                    "Basic facilities available",
                    "Focus on core subjects",
                    "Supportive management",
                    "Regular parent-teacher meetings"
                ],
                reviews: [
                    { author: "Suresh Kumar", rating: 2, text: "Average college for engineering. Affordable option." },
                    { author: "Manju Devi", rating: 2, text: "Basic infrastructure. Need better facilities." }
                ]
            },
            {
                name: "Global Institute of Technology & Management",
                minPercentage: 55,
                interests: ["Engineering", "Management"],
                specificKeywords: ["industry interactions", "student clubs", "sports"],
                courses: ["B.Tech", "MBA", "BBA", "M.Tech"],
                yearlyPrograms: ["Management Conclave", "Engineering Expo", "Cultural Night"],
                highlights: [
                    "Growing institution",
                    "Modern classrooms",
                    "Industry interaction programs",
                    "Active student clubs",
                    "Sports facilities"
                ],
                reviews: [
                    { author: "Ashish Verma", rating: 3, text: "Decent college with improving infrastructure." },
                    { author: "Priyanka Singh", rating: 3, text: "Good campus environment. Faculty is cooperative." }
                ]
            },
            {
                name: "BBD University Kanpur Campus",
                minPercentage: 56,
                interests: ["Engineering", "Management", "Pharmacy"],
                specificKeywords: ["cultural events", "placement assistance", "labs"],
                courses: ["B.Tech", "MBA", "B.Pharma", "BBA"],
                yearlyPrograms: ["University Fest", "Pharma Symposium", "Placement Drive"],
                highlights: [
                    "University campus in Kanpur",
                    "Multiple program options",
                    "Good infrastructure",
                    "Regular cultural events",
                    "Placement assistance"
                ],
                reviews: [
                    { author: "Mohit Agarwal", rating: 3, text: "Good university campus. Variety of courses available." },
                    { author: "Seema Mishra", rating: 3, text: "Decent education quality. Campus life is good." }
                ]
            },
            {
                name: "MVN University Kanpur Center",
                minPercentage: 57,
                interests: ["Engineering", "Management"],
                specificKeywords: ["workshops", "industry partnerships", "placements"],
                courses: ["B.Tech", "MBA", "BCA", "MCA"],
                yearlyPrograms: ["Innovation Week", "Leadership Summit", "Tech Hackathon"],
                highlights: [
                    "Part of MVN education group",
                    "Modern infrastructure",
                    "Industry partnerships",
                    "Regular workshops",
                    "Good placement support"
                ],
                reviews: [
                    { author: "Anuj Sharma", rating: 3, text: "Good college with brand value. Faculty is experienced." },
                    { author: "Ruchi Gupta", rating: 3, text: "Decent college. Placements are satisfactory." }
                ]
            },
            {
                name: "Subharti University Kanpur Extension",
                minPercentage: 58,
                interests: ["Medical", "Engineering", "Pharmacy"],
                specificKeywords: ["clinical exposure", "research", "hospital facilities"],
                courses: ["MBBS", "B.Tech", "B.Pharma", "BDS"],
                yearlyPrograms: ["Medical Conference", "Engineering Seminar", "Health Camp"],
                highlights: [
                    "Medical and technical education",
                    "Well-equipped labs",
                    "Experienced faculty",
                    "Hospital facilities",
                    "Research opportunities"
                ],
                reviews: [
                    { author: "Dr. Amit Singh", rating: 4, text: "Good for medical students. Clinical exposure is excellent." },
                    { author: "Shruti Pandey", rating: 3, text: "Decent college with multiple course options." }
                ]
            },
            {
                name: "Noida International University Kanpur Campus",
                minPercentage: 56,
                interests: ["Engineering", "Management", "Law"],
                specificKeywords: ["guest lectures", "international collaborations", "placements"],
                courses: ["B.Tech", "MBA", "LL.B", "BBA"],
                yearlyPrograms: ["Law Moot Court", "Business Fair", "Global Forum"],
                highlights: [
                    "Multi-disciplinary university campus",
                    "Modern facilities",
                    "International collaborations",
                    "Regular guest lectures",
                    "Active placement cell"
                ],
                reviews: [
                    { author: "Sanjay Mishra", rating: 3, text: "Good university campus. Variety of courses." },
                    { author: "Neetu Verma", rating: 3, text: "Decent infrastructure. Faculty is supportive." }
                ]
            },
            {
                name: "Amity University Kanpur Campus",
                minPercentage: 65,
                interests: ["Engineering", "Management", "Law", "Arts"],
                specificKeywords: ["international exposure", "industry connections", "placements"],
                courses: ["B.Tech", "MBA", "LL.B", "BA LLB", "BBA", "B.Com"],
                yearlyPrograms: ["Amity Youth Fest", "Career Fair", "Art Exhibition"],
                highlights: [
                    "Renowned Amity brand",
                    "World-class infrastructure",
                    "International exposure programs",
                    "Strong industry connections",
                    "Excellent placement record"
                ],
                reviews: [
                    { author: "Raghav Khanna", rating: 4, text: "Excellent college with great brand value. Expensive but worth it." },
                    { author: "Aisha Khan", rating: 4, text: "Best infrastructure and faculty. Great campus life." }
                ]
            },
            {
                name: "Bennett University Kanpur Extension",
                minPercentage: 70,
                interests: ["Engineering", "Management", "Computer"],
                specificKeywords: ["media focus", "tech collaborations", "placements"],
                courses: ["B.Tech", "MBA", "BBA", "B.Sc (Hons)"],
                yearlyPrograms: ["Media Conclave", "Tech Summit", "Innovation Challenge"],
                highlights: [
                    "Part of Times of India group",
                    "World-class facilities",
                    "Media and tech focus",
                    "Strong placement support",
                    "International collaborations"
                ],
                reviews: [
                    { author: "Aryan Gupta", rating: 4, text: "Premium college with excellent facilities. Good for tech and media." },
                    { author: "Ishita Sharma", rating: 4, text: "Expensive but provides great exposure and opportunities." }
                ]
            },
            {
                name: "Lovely Professional University Study Center Kanpur",
                minPercentage: 55,
                interests: ["Engineering", "Management", "Commerce", "Arts"],
                specificKeywords: ["flexible learning", "recognized degrees", "support"],
                courses: ["B.Tech", "MBA", "BBA", "B.Com", "BA"],
                yearlyPrograms: ["LPU Fest", "Commerce Meet", "Arts Festival"],
                highlights: [
                    "Distance and regular programs",
                    "Affordable education",
                    "Recognized degrees",
                    "Flexible learning options",
                    "Support center facilities"
                ],
                reviews: [
                    { author: "Vishal Tiwari", rating: 3, text: "Good for distance education. LPU brand helps in placements." },
                    { author: "Mamta Agarwal", rating: 3, text: "Affordable option with recognized degrees." }
                ]
            },
            {
                name: "Mangalayatan University Kanpur Campus",
                minPercentage: 54,
                interests: ["Engineering", "Management", "Commerce"],
                specificKeywords: ["skill development", "workshops", "placements"],
                courses: ["B.Tech", "MBA", "BBA", "B.Com"],
                yearlyPrograms: ["Skill Fest", "Business Workshop", "Commerce Day"],
                highlights: [
                    "Growing university campus",
                    "Modern infrastructure",
                    "Focus on skill development",
                    "Regular workshops",
                    "Placement assistance"
                ],
                reviews: [
                    { author: "Karan Verma", rating: 3, text: "Developing university. Infrastructure is improving." },
                    { author: "Nikita Singh", rating: 3, text: "Decent college with potential for growth." }
                ]
            },
            {
                name: "Invertis University Kanpur Extension",
                minPercentage: 56,
                interests: ["Engineering", "Management", "Pharmacy"],
                specificKeywords: ["fests", "student communities", "partnerships"],
                courses: ["B.Tech", "MBA", "B.Pharma", "BCA"],
                yearlyPrograms: ["Cultural Fest", "Pharma Expo", "Management Meet"],
                highlights: [
                    "Multi-disciplinary university",
                    "Good infrastructure",
                    "Industry partnerships",
                    "Regular fests and events",
                    "Active student communities"
                ],
                reviews: [
                    { author: "Aditya Pandey", rating: 3, text: "Good university with variety of courses. Campus is nice." },
                    { author: "Tanvi Mishra", rating: 3, text: "Decent education quality. Faculty is experienced." }
                ]
            },
            {
                name: "Sharda University Kanpur Campus",
                minPercentage: 62,
                interests: ["Engineering", "Management", "Medical"],
                specificKeywords: ["international exposure", "research", "placements"],
                courses: ["B.Tech", "MBA", "MBBS", "BDS", "B.Pharma"],
                yearlyPrograms: ["Global Summit", "Medical Conference", "Tech Fest"],
                highlights: [
                    "Renowned university brand",
                    "International exposure",
                    "Modern facilities",
                    "Strong placement record",
                    "Research opportunities"
                ],
                reviews: [
                    { author: "Shubham Agarwal", rating: 4, text: "Premium university with excellent facilities. Good for medical and engineering." },
                    { author: "Aditi Sharma", rating: 4, text: "Expensive but provides world-class education and exposure." }
                ]
            },
            {
                name: "GLA University Kanpur Study Center",
                minPercentage: 60,
                interests: ["Engineering", "Management"],
                specificKeywords: ["workshops", "connections", "placements"],
                courses: ["B.Tech", "MBA", "BCA", "MCA"],
                yearlyPrograms: ["Academic Workshop", "Industry Day", "Placement Week"],
                highlights: [
                    "Established university brand",
                    "Good academic reputation",
                    "Industry connections",
                    "Regular workshops",
                    "Placement support"
                ],
                reviews: [
                    { author: "Aman Singh", rating: 3, text: "Good university with strong academics. Faculty is experienced." },
                    { author: "Parul Gupta", rating: 3, text: "Decent college with good placement support." }
                ]
            },
            {
                name: "Teerthanker Mahaveer University Kanpur Campus",
                minPercentage: 58,
                interests: ["Engineering", "Medical", "Management"],
                specificKeywords: ["research facilities", "placements", "labs"],
                courses: ["B.Tech", "MBBS", "MBA", "B.Pharma"],
                yearlyPrograms: ["Research Day", "Medical Fest", "Business Seminar"],
                highlights: [
                    "Multi-disciplinary university",
                    "Medical and engineering programs",
                    "Good infrastructure",
                    "Research facilities",
                    "Active placement cell"
                ],
                reviews: [
                    { author: "Varun Mishra", rating: 3, text: "Good university with multiple options. Infrastructure is developing." },
                    { author: "Swati Verma", rating: 3, text: "Decent education quality across programs." }
                ]
            },
            {
                name: "IIMT University Kanpur Extension",
                minPercentage: 55,
                interests: ["Engineering", "Management", "Pharmacy"],
                specificKeywords: ["skill programs", "partnerships", "placements"],
                courses: ["B.Tech", "MBA", "B.Pharma", "BCA"],
                yearlyPrograms: ["Skill Development Camp", "Pharma Week", "Tech Meet"],
                highlights: [
                    "Growing university presence",
                    "Modern labs and facilities",
                    "Industry partnerships",
                    "Regular skill development programs",
                    "Placement assistance"
                ],
                reviews: [
                    { author: "Nikhil Jain", rating: 3, text: "Developing university. Good for engineering students." },
                    { author: "Anjali Mishra", rating: 3, text: "Decent facilities. Faculty is supportive." }
                ]
            },
            {
                name: "Shri Venkateshwara University Kanpur Center",
                minPercentage: 56,
                interests: ["Engineering", "Management", "Commerce"],
                specificKeywords: ["guidance sessions", "flexible options", "support"],
                courses: ["B.Tech", "MBA", "BBA", "B.Com"],
                yearlyPrograms: ["Guidance Seminar", "Commerce Fest", "Engineering Day"],
                highlights: [
                    "University study center",
                    "Flexible learning options",
                    "Recognized degrees",
                    "Support facilities",
                    "Regular guidance sessions"
                ],
                reviews: [
                    { author: "Rohit Pandey", rating: 3, text: "Good for working professionals. Flexible schedules." },
                    { author: "Meena Agarwal", rating: 3, text: "Decent option for distance education with support." }
                ]
            },
            {
                name: "Integral University Kanpur Campus",
                minPercentage: 60,
                interests: ["Engineering", "Management", "Pharmacy"],
                specificKeywords: ["research focus", "infrastructure", "placements"],
                courses: ["B.Tech", "MBA", "B.Pharma", "M.Tech"],
                yearlyPrograms: ["Research Symposium", "Pharma Conference", "Tech Fest"],
                highlights: [
                    "Established university campus",
                    "Good academic reputation",
                    "Modern infrastructure",
                    "Research focus",
                    "Decent placement record"
                ],
                reviews: [
                    { author: "Faisal Khan", rating: 3, text: "Good university with quality education. Faculty is knowledgeable." },
                    { author: "Zara Ahmed", rating: 3, text: "Decent college with focus on academics." }
                ]
            },
            {
                name: "Era University Kanpur Extension",
                minPercentage: 62,
                interests: ["Medical", "Engineering", "Management"],
                specificKeywords: ["clinical exposure", "labs", "faculty"],
                courses: ["MBBS", "BDS", "B.Tech", "MBA", "B.Pharma"],
                yearlyPrograms: ["Clinical Workshop", "Engineering Expo", "Management Summit"],
                highlights: [
                    "Medical university with tech programs",
                    "Hospital facilities",
                    "Modern labs",
                    "Experienced medical faculty",
                    "Clinical exposure"
                ],
                reviews: [
                    { author: "Dr. Priya Singh", rating: 4, text: "Good for medical students. Clinical training is thorough." },
                    { author: "Akash Verma", rating: 3, text: "Decent university with multiple program options." }
                ]
            },
            {
                name: "Monad University Kanpur Study Center",
                minPercentage: 54,
                interests: ["Engineering", "Management", "Arts"],
                specificKeywords: ["flexible learning", "affordable", "support"],
                courses: ["B.Tech", "MBA", "BBA", "BA", "B.Com"],
                yearlyPrograms: ["Arts Festival", "Management Day", "Engineering Meet"],
                highlights: [
                    "University study center",
                    "Multiple program options",
                    "Flexible learning",
                    "Support facilities",
                    "Affordable fees"
                ],
                reviews: [
                    { author: "Sachin Gupta", rating: 3, text: "Good for distance learning. Support center is helpful." },
                    { author: "Kritika Sharma", rating: 3, text: "Decent option for working students." }
                ]
            },
            {
                name: "Wisdom School of Management",
                minPercentage: 58,
                interests: ["Management"],
                specificKeywords: ["corporate visits", "case studies", "development"],
                courses: ["BBA", "MBA", "PGDM"],
                yearlyPrograms: ["Corporate Conclave", "Case Study Competition", "Leadership Camp"],
                highlights: [
                    "Management focused institution",
                    "Industry-oriented curriculum",
                    "Regular corporate visits",
                    "Case study methodology",
                    "Personality development focus"
                ],
                reviews: [
                    { author: "Kunal Jain", rating: 3, text: "Good for management students. Faculty has corporate experience." },
                    { author: "Simran Kapoor", rating: 3, text: "Decent management college with practical approach." }
                ]
            },
            {
                name: "Excel Engineering College",
                minPercentage: 52,
                interests: ["Engineering"],
                specificKeywords: ["lab sessions", "workshops", "faculty support"],
                courses: ["B.Tech", "Diploma in Engineering"],
                yearlyPrograms: ["Lab Expo", "Engineering Workshop", "Freshers Meet"],
                highlights: [
                    "Focus on engineering education",
                    "Regular lab sessions",
                    "Workshop facilities",
                    "Affordable fees",
                    "Supportive faculty"
                ],
                reviews: [
                    { author: "Pawan Kumar", rating: 3, text: "Budget engineering college. Good for average students." },
                    { author: "Sunita Mishra", rating: 2, text: "Average infrastructure. Need better facilities." }
                ]
            },
            {
                name: "Kanpur College of Pharmacy",
                minPercentage: 56,
                interests: ["Pharmacy"],
                specificKeywords: ["pharma labs", "industry training", "research"],
                courses: ["B.Pharma", "M.Pharma", "D.Pharma"],
                yearlyPrograms: ["Pharma Fest", "Industry Visit Day", "Research Seminar"],
                highlights: [
                    "Specialized pharmacy college",
                    "Well-equipped pharmaceutical labs",
                    "Industry training programs",
                    "Research opportunities",
                    "Placement in pharma companies"
                ],
                reviews: [
                    { author: "Naveen Pandey", rating: 3, text: "Good for pharmacy students. Practical training is emphasized." },
                    { author: "Roshni Verma", rating: 3, text: "Decent pharmacy college with good lab facilities." }
                ]
            },
            {
                name: "Lakshmi Narain College of Technology & Science",
                minPercentage: 54,
                interests: ["Engineering", "Science"],
                specificKeywords: ["science events", "research", "labs"],
                courses: ["B.Tech", "B.Sc", "M.Tech", "M.Sc"],
                yearlyPrograms: ["Science Fair", "Tech Symposium", "Research Day"],
                highlights: [
                    "Technical and science education",
                    "Good lab facilities",
                    "Research opportunities",
                    "Experienced faculty",
                    "Regular science events"
                ],
                reviews: [
                    { author: "Ashok Yadav", rating: 3, text: "Good for science and engineering. Faculty is supportive." },
                    { author: "Rachna Singh", rating: 3, text: "Decent college with focus on research." }
                ]
            },
            {
                name: "Northern India Engineering College",
                minPercentage: 53,
                interests: ["Engineering"],
                specificKeywords: ["industrial visits", "workshops", "placements"],
                courses: ["B.Tech in CSE", "B.Tech in ME", "B.Tech in Civil", "B.Tech in EE"],
                yearlyPrograms: ["Industrial Tour", "Engineering Fest", "Placement Week"],
                highlights: [
                    "Established engineering college",
                    "Focus on practical knowledge",
                    "Regular industrial visits",
                    "Workshop facilities",
                    "Placement assistance"
                ],
                reviews: [
                    { author: "Sanjiv Kumar", rating: 3, text: "Average engineering college. Faculty tries to help students." },
                    { author: "Pooja Agarwal", rating: 3, text: "Decent option for engineering at affordable cost." }
                ]
            },
            {
                name: "Modern Institute of Technology & Research Centre",
                minPercentage: 55,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["coding workshops", "tech community", "mentorship"],
                courses: ["B.Tech", "M.Tech", "BCA", "MCA"],
                yearlyPrograms: ["Coding Hackathon", "Tech Fest", "Mentor Meet"],
                highlights: [
                    "Modern infrastructure",
                    "IT focused programs",
                    "Regular coding workshops",
                    "Industry mentorship",
                    "Active tech community"
                ],
                reviews: [
                    { author: "Tarun Gupta", rating: 3, text: "Good for IT students. Labs are well-equipped." },
                    { author: "Neha Rastogi", rating: 3, text: "Decent college with focus on technology." }
                ]
            },
            {
                name: "Maharana Pratap Engineering College",
                minPercentage: 52,
                interests: ["Engineering"],
                specificKeywords: ["practicals", "management support", "core subjects"],
                courses: ["B.Tech", "Diploma in Engineering"],
                yearlyPrograms: ["Practical Lab Day", "Core Subject Seminar", "Annual Meet"],
                highlights: [
                    "Budget-friendly engineering education",
                    "Basic facilities",
                    "Focus on core subjects",
                    "Regular practicals",
                    "Supportive management"
                ],
                reviews: [
                    { author: "Dinesh Yadav", rating: 2, text: "Average college for engineering. Affordable option." },
                    { author: "Kamla Devi", rating: 2, text: "Basic infrastructure. Need improvement in facilities." }
                ]
            },
            {
                name: "Institute of Technology & Science (ITS) Kanpur",
                minPercentage: 57,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["tech events", "partnerships", "placements"],
                courses: ["B.Tech", "M.Tech", "BCA", "MCA"],
                yearlyPrograms: ["Tech Event", "Innovation Fair", "Placement Drive"],
                highlights: [
                    "Technology focused institution",
                    "Modern computer labs",
                    "Regular tech events",
                    "Industry partnerships",
                    "Active placement cell"
                ],
                reviews: [
                    { author: "Anshul Sharma", rating: 3, text: "Good college for CSE and IT. Faculty encourages innovation." },
                    { author: "Isha Mishra", rating: 3, text: "Decent infrastructure. Placements are satisfactory." }
                ]
            },
            {
                name: "Alpine Institute of Technology",
                minPercentage: 53,
                interests: ["Engineering"],
                specificKeywords: ["practical training", "industrial exposure", "affordable"],
                courses: ["B.Tech", "Diploma in Engineering"],
                yearlyPrograms: ["Training Workshop", "Industry Day", "Sports Meet"],
                highlights: [
                    "Growing engineering institute",
                    "Focus on practical training",
                    "Workshop facilities",
                    "Industrial exposure",
                    "Affordable fees"
                ],
                reviews: [
                    { author: "Vivek Singh", rating: 3, text: "Developing college. Faculty is cooperative." },
                    { author: "Sapna Gupta", rating: 3, text: "Average college with basic facilities." }
                ]
            },
            {
                name: "Future Institute of Engineering & Technology",
                minPercentage: 54,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["tech workshops", "expert sessions", "training"],
                courses: ["B.Tech in CSE", "B.Tech in IT", "B.Tech in ECE", "M.Tech"],
                yearlyPrograms: ["Future Tech Workshop", "Expert Talk", "Placement Training"],
                highlights: [
                    "Future-ready curriculum",
                    "Modern labs",
                    "Regular tech workshops",
                    "Industry expert sessions",
                    "Placement training"
                ],
                reviews: [
                    { author: "Arun Pandey", rating: 3, text: "Good college with focus on new technologies. Faculty is updated." },
                    { author: "Divya Verma", rating: 3, text: "Decent engineering college. Infrastructure is improving." }
                ]
            },
            {
                name: "Progressive Education Society's College of Engineering",
                minPercentage: 56,
                interests: ["Engineering"],
                specificKeywords: ["industrial training", "quality education", "labs"],
                courses: ["B.Tech", "M.Tech"],
                yearlyPrograms: ["Industrial Training Camp", "Quality Seminar", "Lab Day"],
                highlights: [
                    "Established educational society",
                    "Focus on quality education",
                    "Experienced faculty",
                    "Good lab facilities",
                    "Regular industrial training"
                ],
                reviews: [
                    { author: "Ramesh Tiwari", rating: 3, text: "Good engineering college with experienced teachers." },
                    { author: "Usha Singh", rating: 3, text: "Decent college. Management is supportive." }
                ]
            },
            {
                name: "Indian Institute of Technology (IIT) Kanpur",
                minPercentage: 90,
                interests: ["Engineering", "Science", "Computer"],
                specificKeywords: ["research", "experiments", "internships", "global programs"],
                courses: ["B.Tech in CSE", "B.Tech in Mechanical", "B.Tech in Electrical", "B.Tech in Civil", "M.Tech", "PhD Programs"],
                yearlyPrograms: ["Techkriti", "Rendezvous", "Research Symposium"],
                highlights: [
                    "Premier institute with global recognition",
                    "World-class research facilities",
                    "Excellent placement record with top tech companies",
                    "Beautiful 1000+ acre campus",
                    "Strong alumni network including industry leaders"
                ],
                reviews: [
                    { author: "Rahul Sharma", rating: 5, text: "Best engineering college in India. The faculty and research opportunities are unmatched." },
                    { author: "Priya Singh", rating: 5, text: "Life-changing experience. The campus culture and academic rigor prepare you for anything." }
                ]
            },
            {
                name: "Harcourt Butler Technical University (HBTU)",
                minPercentage: 75,
                interests: ["Engineering", "Computer", "Architecture"],
                specificKeywords: ["coding clubs", "tech societies", "placements"],
                courses: ["B.Tech in CSE", "B.Tech in IT", "B.Tech in Mechanical", "B.Arch", "M.Tech", "MBA"],
                yearlyPrograms: ["Coding Fest", "Architecture Expo", "Cultural Fest"],
                highlights: [
                    "One of the oldest technical institutions in UP",
                    "Strong industry connections",
                    "Affordable quality education",
                    "Active coding clubs and tech societies",
                    "Good placement opportunities"
                ],
                reviews: [
                    { author: "Amit Kumar", rating: 4, text: "Great college with decent placements. The peer group is very competitive and motivating." },
                    { author: "Neha Gupta", rating: 4, text: "Good infrastructure and experienced faculty. Cultural fests are amazing!" }
                ]
            },
            {
                name: "PSIT (Pranveer Singh Institute of Technology)",
                minPercentage: 60,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["guest lectures", "placement cell", "sports"],
                courses: ["B.Tech in CSE", "B.Tech in IT", "B.Tech in ECE", "B.Tech in Mechanical", "MBA", "MCA"],
                yearlyPrograms: ["Guest Lecture Series", "Sports Day", "Tech Fest"],
                highlights: [
                    "Modern infrastructure with AC labs",
                    "Industry-oriented curriculum",
                    "Regular guest lectures by industry experts",
                    "Active placement cell",
                    "Sports and cultural facilities"
                ],
                reviews: [
                    { author: "Vikram Yadav", rating: 4, text: "Good college for CSE. Placements are decent with companies like TCS, Wipro visiting regularly." },
                    { author: "Anjali Verma", rating: 3, text: "Infrastructure is good but need more industry exposure programs." }
                ]
            },
            {
                name: "Axis Colleges",
                minPercentage: 55,
                interests: ["Engineering", "Computer", "Management"],
                specificKeywords: ["practical learning", "entrepreneurship", "visits"],
                courses: ["B.Tech in CSE", "B.Tech in ME", "BBA", "MBA", "B.Pharma"],
                yearlyPrograms: ["Entrepreneur Meet", "Practical Lab Day", "Industrial Visit"],
                highlights: [
                    "Multi-disciplinary institution",
                    "Focus on practical learning",
                    "Entrepreneurship development programs",
                    "Modern computer labs",
                    "Regular industrial visits"
                ],
                reviews: [
                    { author: "Rohit Malhotra", rating: 3, text: "Decent college for engineering. Faculty is supportive and helpful." },
                    { author: "Shreya Agarwal", rating: 4, text: "Good environment for overall development. Extracurricular activities are encouraged." }
                ]
            },
            {
                name: "AKG Engineering College",
                minPercentage: 58,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["coding culture", "hackathons", "placements"],
                courses: ["B.Tech in CSE", "B.Tech in IT", "B.Tech in ECE", "B.Tech in Civil", "MBA"],
                yearlyPrograms: ["Hackathon", "Coding Competition", "Placement Fair"],
                highlights: [
                    "Well-equipped laboratories",
                    "Experienced faculty from IITs and NITs",
                    "Active coding culture",
                    "Regular hackathons and tech events",
                    "Growing placement record"
                ],
                reviews: [
                    { author: "Manish Tiwari", rating: 4, text: "Great for CSE students. Lots of coding competitions and workshops." },
                    { author: "Pooja Mishra", rating: 3, text: "Good college with improving placements year by year." }
                ]
            },
            {
                name: "Ganesh Shankar Vidyarthi Memorial Medical College (GSVM)",
                minPercentage: 88,
                interests: ["Medical"],
                specificKeywords: ["clinical exposure", "hospital", "PG success"],
                courses: ["MBBS", "MD", "MS", "Diploma Courses"],
                yearlyPrograms: ["Medical Conference", "Clinical Workshop", "Alumni Meet"],
                highlights: [
                    "Government medical college with low fees",
                    "Attached to major teaching hospital",
                    "Excellent clinical exposure",
                    "Experienced medical faculty",
                    "Good PG entrance success rate"
                ],
                reviews: [
                    { author: "Dr. Ankit Pandey", rating: 5, text: "Best medical college in Kanpur. Great patient exposure and learning opportunities." },
                    { author: "Dr. Divya Saxena", rating: 4, text: "Challenging environment that makes you a confident doctor. Hostel life is memorable." }
                ]
            },
            {
                name: "Rama Medical College",
                minPercentage: 75,
                interests: ["Medical"],
                specificKeywords: ["research", "CME programs", "faculty ratio"],
                courses: ["MBBS", "BDS", "B.Sc Nursing", "Paramedical Courses"],
                yearlyPrograms: ["Research Day", "CME Seminar", "Nursing Fest"],
                highlights: [
                    "Private medical college with modern facilities",
                    "Well-equipped hospital with 1000+ beds",
                    "Research opportunities available",
                    "Regular CME programs",
                    "Good faculty-student ratio"
                ],
                reviews: [
                    { author: "Kritika Sharma", rating: 4, text: "Good infrastructure and patient variety. Faculty is supportive." },
                    { author: "Varun Gupta", rating: 4, text: "Expensive but worth it for quality medical education." }
                ]
            },
            {
                name: "Institute of Management Studies (IMS) Kanpur",
                minPercentage: 70,
                interests: ["Management"],
                specificKeywords: ["corporate interactions", "case studies", "clubs"],
                courses: ["MBA", "PGDM", "BBA", "Executive MBA"],
                yearlyPrograms: ["Corporate Meet", "Case Study Fest", "Management Club Event"],
                highlights: [
                    "Strong industry interface",
                    "Regular corporate interactions",
                    "Case study based learning",
                    "Good placement in marketing and finance",
                    "Active management clubs"
                ],
                reviews: [
                    { author: "Saurabh Jain", rating: 4, text: "Great for MBA. Good mix of academics and practical exposure." },
                    { author: "Megha Kapoor", rating: 4, text: "Faculty has industry experience. Placements are satisfactory." }
                ]
            },
            {
                name: "Lloyd Business School",
                minPercentage: 65,
                interests: ["Management"],
                specificKeywords: ["industrial training", "entrepreneurship", "collaborations"],
                courses: ["BBA", "MBA", "PGDM", "B.Com Hons"],
                yearlyPrograms: ["Training Camp", "Entrepreneur Fair", "International Day"],
                highlights: [
                    "Modern campus with AC classrooms",
                    "Focus on personality development",
                    "Regular industrial training",
                    "International collaborations",
                    "Active entrepreneurship cell"
                ],
                reviews: [
                    { author: "Arjun Khanna", rating: 3, text: "Good for BBA. Lots of events and competitions throughout the year." },
                    { author: "Simran Chopra", rating: 4, text: "Faculty is experienced. Practical approach to management education." }
                ]
            },
            {
                name: "Chandra Shekhar Azad University of Agriculture & Technology (CSAUAT)",
                minPercentage: 60,
                interests: ["Commerce", "Management", "Science"],
                specificKeywords: ["agricultural research", "peaceful campus", "placements"],
                courses: ["B.Com", "M.Com", "MBA", "B.Sc Agriculture", "M.Sc"],
                yearlyPrograms: ["Agriculture Fair", "Commerce Seminar", "Science Day"],
                highlights: [
                    "Government university with low fees",
                    "Good for commerce students",
                    "Agricultural research opportunities",
                    "Peaceful campus environment",
                    "Decent placement assistance"
                ],
                reviews: [
                    { author: "Naman Agarwal", rating: 3, text: "Good government college for B.Com. Affordable and decent education." },
                    { author: "Ritu Singh", rating: 3, text: "Campus is nice but placements could be better." }
                ]
            },
            {
                name: "DAV College Kanpur",
                minPercentage: 55,
                interests: ["Commerce", "Arts", "Science"],
                specificKeywords: ["NCC", "NSS", "cultural programs"],
                courses: ["B.Com", "B.A.", "B.Sc", "M.Com", "M.A."],
                yearlyPrograms: ["Cultural Program", "NCC Camp", "NSS Drive"],
                highlights: [
                    "Established institution with good reputation",
                    "Affordable fees structure",
                    "Good faculty for commerce",
                    "Active NCC and NSS units",
                    "Regular cultural programs"
                ],
                reviews: [
                    { author: "Gaurav Mishra", rating: 4, text: "One of the best colleges for B.Com in Kanpur. Faculty is very knowledgeable." },
                    { author: "Sakshi Gupta", rating: 4, text: "Great college life. Teachers are supportive and encouraging." }
                ]
            },
            {
                name: "Christ Church College",
                minPercentage: 50,
                interests: ["Commerce", "Arts"],
                specificKeywords: ["debate societies", "literary", "holistic development"],
                courses: ["B.Com", "B.A.", "M.Com", "M.A. in English"],
                yearlyPrograms: ["Debate Competition", "Literary Fest", "Arts Day"],
                highlights: [
                    "Historic institution with legacy",
                    "Focus on holistic development",
                    "Good for arts and commerce",
                    "Active debate and literary societies",
                    "Centrally located campus"
                ],
                reviews: [
                    { author: "Ayush Verma", rating: 3, text: "Good college for arts students. Faculty is experienced." },
                    { author: "Isha Sharma", rating: 3, text: "Nice environment for studies. Need better infrastructure." }
                ]
            },
            {
                name: "Institute of Engineering & Technology (IET) Kanpur",
                minPercentage: 68,
                interests: ["Computer", "Engineering"],
                specificKeywords: ["coding community", "technical training", "placements"],
                courses: ["BCA", "MCA", "B.Tech", "M.Tech"],
                yearlyPrograms: ["Coding Fest", "Tech Training", "Placement Week"],
                highlights: [
                    "Government institute under AKTU",
                    "Low fees with quality education",
                    "Strong technical training",
                    "Active coding community",
                    "Good placement record"
                ],
                reviews: [
                    { author: "Shubham Rai", rating: 4, text: "Best government college for MCA. Great faculty and infrastructure." },
                    { author: "Pallavi Joshi", rating: 4, text: "Excellent for computer science students. Peer learning is great." }
                ]
            },
            {
                name: "Babu Banarasi Das University (BBDU)",
                minPercentage: 55,
                interests: ["Computer", "Engineering", "Management"],
                specificKeywords: ["skill workshops", "alumni network", "IT infrastructure"],
                courses: ["BCA", "MCA", "B.Tech", "MBA", "B.Pharma"],
                yearlyPrograms: ["Skill Workshop", "Alumni Meet", "IT Day"],
                highlights: [
                    "Private university with multiple programs",
                    "Modern IT infrastructure",
                    "Industry partnerships",
                    "Regular skill development workshops",
                    "Growing alumni network"
                ],
                reviews: [
                    { author: "Karan Singh", rating: 3, text: "Good for BCA. Faculty is supportive. Need better placements." },
                    { author: "Prachi Agarwal", rating: 3, text: "Decent college with good facilities. Improving every year." }
                ]
            },
            {
                name: "Kanpur University (CSJM University)",
                minPercentage: 50,
                interests: ["Arts", "Commerce", "Science"],
                specificKeywords: ["research opportunities", "wide courses", "affordable"],
                courses: ["B.A.", "M.A.", "B.Com", "M.Com", "B.Sc", "M.Sc", "PhD"],
                yearlyPrograms: ["Arts Seminar", "Commerce Conference", "Science Fest"],
                highlights: [
                    "Main university of Kanpur",
                    "Wide range of courses",
                    "Affordable government institution",
                    "Strong arts and humanities department",
                    "Research opportunities available"
                ],
                reviews: [
                    { author: "Deepak Kumar", rating: 3, text: "Good for arts students. Many affiliated colleges offer variety." },
                    { author: "Sneha Mishra", rating: 3, text: "Decent university for postgraduate studies in arts." }
                ]
            },
            {
                name: "National Law University (NLU) Kanpur",
                minPercentage: 85,
                interests: ["Law"],
                specificKeywords: ["moot courts", "legal research", "placements"],
                courses: ["B.A. LL.B", "LL.M", "PhD in Law"],
                yearlyPrograms: ["Moot Court Competition", "Legal Research Day", "Law Fest"],
                highlights: [
                    "Premier law institution",
                    "Excellent faculty with judicial experience",
                    "Regular moot court competitions",
                    "Strong legal research culture",
                    "Good placement in law firms and corporates"
                ],
                reviews: [
                    { author: "Aditya Mishra", rating: 5, text: "Best law college in the region. Rigorous training prepares you for legal profession." },
                    { author: "Nikita Singh", rating: 4, text: "Challenging but rewarding. Great exposure to legal field." }
                ]
            },
            {
                name: "IFTM University Kanpur Campus",
                minPercentage: 58,
                interests: ["Pharmacy", "Medical"],
                specificKeywords: ["pharma labs", "industrial training", "research"],
                courses: ["B.Pharma", "M.Pharma", "D.Pharma", "Pharm.D"],
                yearlyPrograms: ["Pharma Research Day", "Medical Training", "Lab Workshop"],
                highlights: [
                    "Well-equipped pharmaceutical labs",
                    "Industrial training programs",
                    "Research in pharmaceutical sciences",
                    "Good placement in pharma companies",
                    "Modern infrastructure"
                ],
                reviews: [
                    { author: "Vishal Gupta", rating: 4, text: "Great for pharmacy students. Good practical exposure." },
                    { author: "Anjana Sharma", rating: 3, text: "Decent college with improving placements in pharma sector." }
                ]
            },
            {
                name: "JSS Academy of Technical Education",
                minPercentage: 62,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["technical workshops", "student clubs", "connections"],
                courses: ["B.Tech in CSE", "B.Tech in ME", "B.Tech in ECE", "MBA"],
                yearlyPrograms: ["Technical Workshop", "Club Fest", "Industry Connect"],
                highlights: [
                    "Focus on technical skills",
                    "Modern lab facilities",
                    "Regular technical workshops",
                    "Active student clubs",
                    "Growing industry connections"
                ],
                reviews: [
                    { author: "Rajat Verma", rating: 3, text: "Good college for engineering. Faculty is cooperative." },
                    { author: "Kavya Rastogi", rating: 3, text: "Decent infrastructure. Need more placement drives." }
                ]
            },
            {
                name: "Naraina College of Engineering & Technology",
                minPercentage: 55,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["project exhibitions", "sports", "faculty support"],
                courses: ["B.Tech in CSE", "B.Tech in IT", "B.Tech in Civil", "B.Tech in Mechanical"],
                yearlyPrograms: ["Project Expo", "Sports Day", "Tech Meet"],
                highlights: [
                    "Affordable engineering education",
                    "Practical approach to learning",
                    "Regular project exhibitions",
                    "Sports facilities available",
                    "Supportive faculty"
                ],
                reviews: [
                    { author: "Mohit Sharma", rating: 3, text: "Good for students with average percentage. Teachers help a lot." },
                    { author: "Riya Gupta", rating: 3, text: "Budget-friendly option with decent education quality." }
                ]
            },
            {
                name: "Sri Ram Swaroop Memorial College",
                minPercentage: 52,
                interests: ["Commerce", "Management"],
                specificKeywords: ["CA coaching", "guest lectures", "academic"],
                courses: ["B.Com", "BBA", "M.Com", "MBA"],
                yearlyPrograms: ["CA Prep Session", "Guest Lecture Series", "Commerce Fest"],
                highlights: [
                    "Established commerce college",
                    "Focus on accounting and finance",
                    "CA coaching assistance",
                    "Regular guest lectures",
                    "Good academic environment"
                ],
                reviews: [
                    { author: "Aman Saxena", rating: 4, text: "Best for commerce students preparing for CA. Faculty guides well." },
                    { author: "Priyanka Dwivedi", rating: 3, text: "Good college for B.Com. Helps in competitive exam preparation." }
                ]
            },
            {
                name: "Vidya College of Education",
                minPercentage: 50,
                interests: ["Arts", "Commerce"],
                specificKeywords: ["teaching experience", "pedagogy workshops", "affordable"],
                courses: ["B.Ed", "M.Ed", "D.El.Ed"],
                yearlyPrograms: ["Teaching Practice", "Pedagogy Workshop", "Education Day"],
                highlights: [
                    "Focus on teacher training",
                    "Practical teaching experience",
                    "Good for those wanting teaching career",
                    "Regular workshops on pedagogy",
                    "Affordable fees"
                ],
                reviews: [
                    { author: "Sunita Verma", rating: 4, text: "Excellent for B.Ed students. Teaching practice is well-organized." },
                    { author: "Ramesh Gupta", rating: 4, text: "Great faculty who are experienced teachers themselves." }
                ]
            },
            {
                name: "Government Science College",
                minPercentage: 60,
                interests: ["Science"],
                specificKeywords: ["competitive exams", "science labs", "faculty"],
                courses: ["B.Sc in Physics", "B.Sc in Chemistry", "B.Sc in Maths", "M.Sc"],
                yearlyPrograms: ["Science Competition", "Lab Day", "Exam Prep Camp"],
                highlights: [
                    "Government college with nominal fees",
                    "Good for pure science students",
                    "Well-equipped science labs",
                    "Prepares well for competitive exams",
                    "Experienced science faculty"
                ],
                reviews: [
                    { author: "Abhishek Mishra", rating: 4, text: "Best government college for B.Sc. Great for students preparing for IIT-JAM." },
                    { author: "Swati Singh", rating: 4, text: "Excellent science faculty. Good environment for research-minded students." }
                ]
            },
            {
                name: "Accurate Institute of Management and Technology",
                minPercentage: 58,
                interests: ["Management", "Computer"],
                specificKeywords: ["corporate visits", "personality development", "placements"],
                courses: ["BBA", "BCA", "MBA", "MCA"],
                yearlyPrograms: ["Corporate Visit", "PD Session", "Placement Drive"],
                highlights: [
                    "Focus on industry-ready skills",
                    "Regular corporate visits",
                    "Personality development programs",
                    "Modern campus facilities",
                    "Active placement cell"
                ],
                reviews: [
                    { author: "Siddharth Jain", rating: 3, text: "Good for management studies. Events and competitions are regular." },
                    { author: "Tanya Agarwal", rating: 3, text: "Decent college with focus on overall development." }
                ]
            },
            {
                name: "Kamla Nehru Institute of Technology (KNIT)",
                minPercentage: 72,
                interests: ["Engineering", "Architecture"],
                specificKeywords: ["design studios", "workshops", "placements"],
                courses: ["B.Tech", "B.Arch", "M.Tech"],
                yearlyPrograms: ["Design Workshop", "Architecture Fest", "Tech Day"],
                highlights: [
                    "Government engineering college",
                    "Good for architecture students",
                    "Design studios and workshops",
                    "Experienced architecture faculty",
                    "Decent placement record"
                ],
                reviews: [
                    { author: "Nishant Malhotra", rating: 4, text: "Great for architecture. Good balance of theory and practical work." },
                    { author: "Avni Sharma", rating: 4, text: "Faculty is supportive. Studio culture is very collaborative." }
                ]
            },
            {
                name: "R.V. Northland Institute",
                minPercentage: 55,
                interests: ["Pharmacy", "Engineering", "Management"],
                specificKeywords: ["industrial tie-ups", "guest lectures", "infrastructure"],
                courses: ["B.Pharma", "B.Tech", "MBA", "D.Pharma"],
                yearlyPrograms: ["Tie-up Seminar", "Guest Lecture", "Pharma Day"],
                highlights: [
                    "Multi-disciplinary institution",
                    "Modern pharmacy labs",
                    "Industrial tie-ups",
                    "Regular guest lectures",
                    "Good infrastructure"
                ],
                reviews: [
                    { author: "Piyush Gupta", rating: 3, text: "Good for pharmacy students. Faculty has industry experience." },
                    { author: "Nidhi Verma", rating: 3, text: "Decent college with focus on practical pharmaceutical training." }
                ]
            },
            {
                name: "Shri Ramswaroop Memorial Group of Colleges",
                minPercentage: 60,
                interests: ["Engineering", "Management", "Pharmacy"],
                specificKeywords: ["cultural fests", "training cell", "sports"],
                courses: ["B.Tech", "MBA", "B.Pharma", "MCA"],
                yearlyPrograms: ["Cultural Fest", "Training Session", "Sports Complex Event"],
                highlights: [
                    "Large campus with multiple departments",
                    "Good infrastructure",
                    "Regular cultural and technical fests",
                    "Active training and placement cell",
                    "Sports complex available"
                ],
                reviews: [
                    { author: "Harsh Pandey", rating: 3, text: "Big college with many facilities. Good campus life." },
                    { author: "Richa Agarwal", rating: 3, text: "Decent college for engineering. Placements are improving." }
                ]
            },
            {
                name: "Sanskriti University",
                minPercentage: 52,
                interests: ["Engineering", "Management", "Arts", "Commerce"],
                specificKeywords: ["skill development", "partnerships", "seminars"],
                courses: ["B.Tech", "BBA", "B.Com", "B.A.", "MBA", "M.Tech"],
                yearlyPrograms: ["Skill Seminar", "Partnership Meet", "Arts Day"],
                highlights: [
                    "Private university with multiple programs",
                    "Modern facilities",
                    "Focus on skill development",
                    "Industry partnerships",
                    "Regular workshops and seminars"
                ],
                reviews: [
                    { author: "Akash Tiwari", rating: 3, text: "Good university with variety of courses. Faculty is supportive." },
                    { author: "Pooja Saxena", rating: 3, text: "Developing university with potential. Infrastructure is good." }
                ]
            },
            {
                name: "Radha Govind Engineering College",
                minPercentage: 56,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["coding competitions", "expert sessions", "clubs"],
                courses: ["B.Tech in CSE", "B.Tech in IT", "B.Tech in ECE", "B.Tech in ME"],
                yearlyPrograms: ["Coding Competition", "Expert Session", "Tech Club Meet"],
                highlights: [
                    "Focus on technical education",
                    "Regular coding competitions",
                    "Industry expert sessions",
                    "Well-maintained labs",
                    "Active technical clubs"
                ],
                reviews: [
                    { author: "Vinay Kumar", rating: 3, text: "Good for engineering students. Faculty is experienced." },
                    { author: "Shruti Mishra", rating: 3, text: "Decent college with focus on practical learning." }
                ]
            },
            {
                name: "Bundelkhand Institute of Engineering & Technology",
                minPercentage: 54,
                interests: ["Engineering"],
                specificKeywords: ["industrial training", "core branches", "faculty"],
                courses: ["B.Tech in Civil", "B.Tech in Mechanical", "B.Tech in Electrical", "B.Tech in CSE"],
                yearlyPrograms: ["Industrial Training", "Core Branch Seminar", "Engineering Day"],
                highlights: [
                    "Government aided institution",
                    "Affordable fees structure",
                    "Good for core engineering branches",
                    "Experienced faculty",
                    "Regular industrial training"
                ],
                reviews: [
                    { author: "Rajesh Yadav", rating: 3, text: "Good government college. Strong in mechanical and civil engineering." },
                    { author: "Madhuri Singh", rating: 3, text: "Budget-friendly with decent education quality." }
                ]
            },
            {
                name: "United College of Engineering & Research",
                minPercentage: 53,
                interests: ["Engineering", "Management"],
                specificKeywords: ["personality sessions", "library", "societies"],
                courses: ["B.Tech", "MBA", "Diploma in Engineering"],
                yearlyPrograms: ["PD Session", "Library Week", "Society Event"],
                highlights: [
                    "Multiple engineering branches",
                    "Focus on employability skills",
                    "Regular personality development sessions",
                    "Good library facilities",
                    "Active student societies"
                ],
                reviews: [
                    { author: "Sunil Gupta", rating: 3, text: "Average college but faculty tries hard to help students." },
                    { author: "Anita Sharma", rating: 3, text: "Decent option for engineering at affordable fees." }
                ]
            },
            {
                name: "Maharishi University of Information Technology",
                minPercentage: 55,
                interests: ["Computer", "Engineering"],
                specificKeywords: ["hackathons", "coding culture", "curriculum"],
                courses: ["B.Tech", "BCA", "MCA", "M.Tech"],
                yearlyPrograms: ["Hackathon", "Coding Camp", "IT Seminar"],
                highlights: [
                    "Focus on IT and computer science",
                    "Modern computer labs",
                    "Regular hackathons",
                    "Industry-oriented curriculum",
                    "Coding culture"
                ],
                reviews: [
                    { author: "Deepak Joshi", rating: 3, text: "Good for computer science students. Labs are well-equipped." },
                    { author: "Sapna Verma", rating: 3, text: "Focuses on programming skills. Need better placements." }
                ]
            },
            {
                name: "Galgotias University Kanpur Campus",
                minPercentage: 58,
                interests: ["Engineering", "Management", "Computer"],
                specificKeywords: ["corporate training", "international programs", "connections"],
                courses: ["B.Tech", "BCA", "BBA", "MBA", "M.Tech"],
                yearlyPrograms: ["Corporate Training", "International Day", "Industry Connect"],
                highlights: [
                    "Part of renowned Galgotias group",
                    "Modern infrastructure",
                    "Good industry connections",
                    "Regular corporate training",
                    "International exposure programs"
                ],
                reviews: [
                    { author: "Vaibhav Singh", rating: 4, text: "Good college with brand value. Placements are satisfactory." },
                    { author: "Neetu Agarwal", rating: 3, text: "Expensive but provides good facilities and exposure." }
                ]
            },
            {
                name: "Shambhunath Institute of Engineering & Technology",
                minPercentage: 52,
                interests: ["Engineering"],
                specificKeywords: ["guest lectures", "workshop facilities", "management"],
                courses: ["B.Tech in CSE", "B.Tech in ME", "B.Tech in Civil", "B.Tech in EE"],
                yearlyPrograms: ["Guest Lecture", "Workshop Day", "Annual Meet"],
                highlights: [
                    "Affordable engineering college",
                    "Focus on fundamental concepts",
                    "Regular guest lectures",
                    "Good workshop facilities",
                    "Supportive management"
                ],
                reviews: [
                    { author: "Praveen Kumar", rating: 3, text: "Budget college with basic facilities. Teachers are helpful." },
                    { author: "Rekha Mishra", rating: 3, text: "Good for students with limited budget. Education quality is decent." }
                ]
            },
            {
                name: "Technocrats Institute of Technology",
                minPercentage: 54,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["technical workshops", "project learning", "robotics"],
                courses: ["B.Tech", "Diploma in Engineering", "M.Tech"],
                yearlyPrograms: ["Technical Workshop", "Project Exhibition", "Robotics Fest"],
                highlights: [
                    "Technical focused institution",
                    "Regular technical workshops",
                    "Project-based learning",
                    "Industry mentorship programs",
                    "Active robotics club"
                ],
                reviews: [
                    { author: "Sanjay Tiwari", rating: 3, text: "Good for technical skills development. Hands-on approach to learning." },
                    { author: "Priyanka Gupta", rating: 3, text: "Decent college with focus on practical knowledge." }
                ]
            },
            {
                name: "Lucknow Christian Degree College (Kanpur Branch)",
                minPercentage: 50,
                interests: ["Arts", "Commerce"],
                specificKeywords: ["cultural activities", "value education", "campus"],
                courses: ["B.A.", "B.Com", "M.A.", "M.Com"],
                yearlyPrograms: ["Cultural Activity", "Value Education Seminar", "Campus Day"],
                highlights: [
                    "Minority institution with inclusive culture",
                    "Focus on value-based education",
                    "Good for arts and commerce",
                    "Regular cultural activities",
                    "Peaceful campus environment"
                ],
                reviews: [
                    { author: "Thomas Jacob", rating: 3, text: "Good college with focus on character building. Faculty is caring." },
                    { author: "Mary Joseph", rating: 3, text: "Nice environment for studies. Teachers are supportive." }
                ]
            },
            {
                name: "Kanpur Institute of Technology & Pharmacy",
                minPercentage: 55,
                interests: ["Pharmacy", "Engineering"],
                specificKeywords: ["industrial visits", "research", "placements"],
                courses: ["B.Pharma", "D.Pharma", "B.Tech", "M.Pharma"],
                yearlyPrograms: ["Industrial Visit", "Research Day", "Pharma Placement"],
                highlights: [
                    "Combined tech and pharmacy institute",
                    "Well-equipped pharmaceutical labs",
                    "Regular industrial visits",
                    "Focus on research",
                    "Placement assistance"
                ],
                reviews: [
                    { author: "Rohit Pandey", rating: 3, text: "Good for pharmacy students. Practical training is emphasized." },
                    { author: "Seema Verma", rating: 3, text: "Decent college with good lab facilities." }
                ]
            },
            {
                name: "Vivekananda College of Technology & Management",
                minPercentage: 53,
                interests: ["Engineering", "Management"],
                specificKeywords: ["motivational sessions", "sports", "value programs"],
                courses: ["B.Tech", "BBA", "MBA", "Diploma"],
                yearlyPrograms: ["Motivational Talk", "Sports Event", "Value Program"],
                highlights: [
                    "Multi-disciplinary institution",
                    "Focus on holistic development",
                    "Regular motivational sessions",
                    "Sports and cultural activities",
                    "Value education programs"
                ],
                reviews: [
                    { author: "Ankit Dubey", rating: 3, text: "Good college with focus on overall personality. Faculty is supportive." },
                    { author: "Ritu Singh", rating: 3, text: "Decent infrastructure and learning environment." }
                ]
            },
            {
                name: "Buddha Institute of Technology",
                minPercentage: 52,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["lab sessions", "placements", "core subjects"],
                courses: ["B.Tech in CSE", "B.Tech in ECE", "B.Tech in ME", "Diploma"],
                yearlyPrograms: ["Lab Session Day", "Placement Drive", "Core Subject Fest"],
                highlights: [
                    "Growing engineering institute",
                    "Affordable fee structure",
                    "Focus on core subjects",
                    "Regular lab sessions",
                    "Improving placement record"
                ],
                reviews: [
                    { author: "Manoj Kumar", rating: 3, text: "Budget-friendly engineering college. Education quality is acceptable." },
                    { author: "Sonam Gupta", rating: 2, text: "Average college. Need better infrastructure and placements." }
                ]
            },
            {
                name: "Rajarshi Rananjay Singh College",
                minPercentage: 50,
                interests: ["Arts", "Commerce", "Science"],
                specificKeywords: ["competitive prep", "NSS", "affordable"],
                courses: ["B.A.", "B.Sc", "B.Com", "M.A."],
                yearlyPrograms: ["Competitive Exam Prep", "NSS Camp", "Science Day"],
                highlights: [
                    "Affiliated to CSJM University",
                    "Multiple stream options",
                    "Affordable education",
                    "Good for competitive exam preparation",
                    "Active NSS unit"
                ],
                reviews: [
                    { author: "Ajay Verma", rating: 3, text: "Decent college for graduation. Faculty is experienced." },
                    { author: "Geeta Sharma", rating: 3, text: "Good for students looking for affordable education." }
                ]
            },
            {
                name: "Jagran College of Arts, Science & Commerce",
                minPercentage: 52,
                interests: ["Arts", "Commerce", "Science"],
                specificKeywords: ["media courses", "guest lectures", "library"],
                courses: ["B.A.", "B.Com", "B.Sc", "M.A.", "M.Com"],
                yearlyPrograms: ["Media Workshop", "Guest Lecture", "Library Week"],
                highlights: [
                    "Part of Jagran media group",
                    "Modern infrastructure",
                    "Media and communication courses",
                    "Regular guest lectures from journalists",
                    "Good library resources"
                ],
                reviews: [
                    { author: "Shivam Singh", rating: 3, text: "Good college especially for mass communication. Faculty from industry." },
                    { author: "Ankita Mishra", rating: 3, text: "Nice college with focus on media education." }
                ]
            },
            {
                name: "IILM Academy of Higher Learning",
                minPercentage: 60,
                interests: ["Management", "Computer"],
                specificKeywords: ["corporate interactions", "personality focus", "collaborations"],
                courses: ["BBA", "BCA", "MBA"],
                yearlyPrograms: ["Corporate Interaction", "PD Camp", "International Seminar"],
                highlights: [
                    "Focus on management education",
                    "Industry-integrated curriculum",
                    "Regular corporate interactions",
                    "Personality development focus",
                    "International collaborations"
                ],
                reviews: [
                    { author: "Vishal Jain", rating: 3, text: "Good for management students. Faculty has corporate experience." },
                    { author: "Prerna Agarwal", rating: 3, text: "Expensive but provides good exposure to corporate world." }
                ]
            },
            {
                name: "Shri Ramswaroop Memorial University",
                minPercentage: 55,
                interests: ["Engineering", "Management", "Law", "Pharmacy"],
                specificKeywords: ["fests", "competitions", "sports"],
                courses: ["B.Tech", "MBA", "B.Pharma", "LL.B", "LL.M"],
                yearlyPrograms: ["University Fest", "Competition Day", "Sports Meet"],
                highlights: [
                    "Multi-faculty university",
                    "Large campus with various departments",
                    "Regular fests and competitions",
                    "Sports complex",
                    "Active placement cell"
                ],
                reviews: [
                    { author: "Arun Pandey", rating: 3, text: "Big university with many options. Campus life is good." },
                    { author: "Divya Rastogi", rating: 3, text: "Decent university. Placements vary by department." }
                ]
            },
            {
                name: "Dr. Ambedkar Institute of Technology for Handicapped",
                minPercentage: 50,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["inclusive facilities", "support staff", "barrier-free"],
                courses: ["B.Tech", "Diploma in Engineering", "BCA"],
                yearlyPrograms: ["Inclusive Event", "Support Seminar", "Tech Day"],
                highlights: [
                    "Inclusive education institute",
                    "Special facilities for differently-abled",
                    "Government support",
                    "Barrier-free campus",
                    "Supportive faculty and staff"
                ],
                reviews: [
                    { author: "Ramesh Yadav", rating: 4, text: "Excellent initiative for inclusive education. Very supportive environment." },
                    { author: "Sunita Verma", rating: 4, text: "Great college with focus on empowering differently-abled students." }
                ]
            },
            {
                name: "Truba Institute of Engineering & IT",
                minPercentage: 53,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["coding competitions", "tech clubs", "mentorship"],
                courses: ["B.Tech", "M.Tech", "BCA", "MCA"],
                yearlyPrograms: ["Coding Competition", "Club Meet", "Mentor Session"],
                highlights: [
                    "Focus on IT education",
                    "Modern computer infrastructure",
                    "Regular coding competitions",
                    "Industry mentorship",
                    "Active tech clubs"
                ],
                reviews: [
                    { author: "Gaurav Mishra", rating: 3, text: "Good for IT students. Faculty encourages coding culture." },
                    { author: "Neha Gupta", rating: 3, text: "Decent college with focus on technical skills." }
                ]
            },
            {
                name: "Ideal Institute of Management & Technology",
                minPercentage: 54,
                interests: ["Management", "Computer"],
                specificKeywords: ["corporate workshops", "soft skills", "entrepreneurship"],
                courses: ["BBA", "BCA", "MBA", "MCA"],
                yearlyPrograms: ["Workshop Series", "Soft Skills Camp", "Entrepreneur Day"],
                highlights: [
                    "Management and IT focused",
                    "Regular corporate workshops",
                    "Soft skills training",
                    "Good library facilities",
                    "Active entrepreneurship cell"
                ],
                reviews: [
                    { author: "Saurabh Jain", rating: 3, text: "Good for BBA and BCA. Faculty is supportive." },
                    { author: "Pallavi Saxena", rating: 3, text: "Decent college with focus on personality development." }
                ]
            },
            {
                name: "Kanpur Institute of Technology",
                minPercentage: 52,
                interests: ["Engineering"],
                specificKeywords: ["lab practicals", "industrial training", "affordable"],
                courses: ["B.Tech in CSE", "B.Tech in ME", "B.Tech in Civil", "B.Tech in EE"],
                yearlyPrograms: ["Lab Practical Day", "Industrial Training", "Engineering Fest"],
                highlights: [
                    "Established engineering institute",
                    "Focus on core engineering",
                    "Regular lab practical sessions",
                    "Industrial training programs",
                    "Affordable fees"
                ],
                reviews: [
                    { author: "Ravi Shankar", rating: 3, text: "Budget engineering college. Good for students with limited resources." },
                    { author: "Kiran Verma", rating: 3, text: "Average college with basic facilities. Faculty tries to help." }
                ]
            },
            {
                name: "Saroj Institute of Technology & Management",
                minPercentage: 53,
                interests: ["Engineering", "Management"],
                specificKeywords: ["industry visits", "student clubs", "sports"],
                courses: ["B.Tech", "MBA", "BBA", "Diploma"],
                yearlyPrograms: ["Industry Visit", "Club Event", "Sports Day"],
                highlights: [
                    "Combined technical and management education",
                    "Regular industry visits",
                    "Focus on practical training",
                    "Active student clubs",
                    "Sports facilities"
                ],
                reviews: [
                    { author: "Nitin Gupta", rating: 3, text: "Good college with variety of courses. Campus is decent." },
                    { author: "Pooja Mishra", rating: 3, text: "Average college. Placements could be better." }
                ]
            },
            {
                name: "GNIOT Greater Noida (Kanpur Extension)",
                minPercentage: 57,
                interests: ["Engineering", "Management"],
                specificKeywords: ["technical fests", "partnerships", "placements"],
                courses: ["B.Tech", "MBA", "BCA", "MCA"],
                yearlyPrograms: ["Technical Fest", "Partnership Seminar", "Placement Week"],
                highlights: [
                    "Extension campus of Greater Noida college",
                    "Good infrastructure",
                    "Industry partnerships",
                    "Regular technical fests",
                    "Decent placement support"
                ],
                reviews: [
                    { author: "Abhishek Singh", rating: 3, text: "Good extension campus. Faculty is experienced." },
                    { author: "Swati Agarwal", rating: 3, text: "Decent college with growing reputation." }
                ]
            },
            {
                name: "Azad Institute of Engineering & Technology",
                minPercentage: 51,
                interests: ["Engineering"],
                specificKeywords: ["workshops", "lab facilities", "support"],
                courses: ["B.Tech", "Diploma in Engineering", "M.Tech"],
                yearlyPrograms: ["Workshop Series", "Lab Day", "Faculty Support Session"],
                highlights: [
                    "Affordable technical education",
                    "Focus on fundamental concepts",
                    "Regular workshops",
                    "Good lab facilities for basic branches",
                    "Supportive faculty"
                ],
                reviews: [
                    { author: "Mukesh Yadav", rating: 3, text: "Budget-friendly engineering college. Good for average students." },
                    { author: "Rani Gupta", rating: 2, text: "Average college. Need better placement opportunities." }
                ]
            },
            {
                name: "Krishna Engineering College",
                minPercentage: 54,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["tech events", "coding community", "labs"],
                courses: ["B.Tech in CSE", "B.Tech in IT", "B.Tech in ECE", "B.Tech in ME"],
                yearlyPrograms: ["Tech Event", "Coding Meet", "Lab Workshop"],
                highlights: [
                    "Growing engineering institution",
                    "Modern labs",
                    "Regular tech events",
                    "Industry expert sessions",
                    "Active coding community"
                ],
                reviews: [
                    { author: "Sumit Verma", rating: 3, text: "Decent engineering college. Faculty is cooperative." },
                    { author: "Ritu Sharma", rating: 3, text: "Good for CSE students. Labs are well-maintained." }
                ]
            },
            {
                name: "Institute of Professional Studies",
                minPercentage: 55,
                interests: ["Management", "Computer"],
                specificKeywords: ["seminars", "industry connections", "soft skills"],
                courses: ["BBA", "BCA", "MBA", "PGDM"],
                yearlyPrograms: ["Professional Seminar", "Industry Connect", "Soft Skills Camp"],
                highlights: [
                    "Professional education focus",
                    "Corporate training programs",
                    "Personality development",
                    "Regular seminars",
                    "Industry connections"
                ],
                reviews: [
                    { author: "Manish Jain", rating: 3, text: "Good for management education. Faculty has industry background." },
                    { author: "Sakshi Mishra", rating: 3, text: "Decent college with focus on soft skills." }
                ]
            },
            {
                name: "Rajkiya Engineering College Kanpur",
                minPercentage: 68,
                interests: ["Engineering"],
                specificKeywords: ["competitive prep", "quality education", "affordable"],
                courses: ["B.Tech", "M.Tech"],
                yearlyPrograms: ["Competitive Exam Camp", "Quality Seminar", "Engineering Day"],
                highlights: [
                    "Government engineering college",
                    "Low fees structure",
                    "Quality technical education",
                    "Experienced faculty",
                    "Good for competitive exam preparation"
                ],
                reviews: [
                    { author: "Anil Kumar", rating: 4, text: "Best government engineering college. Very affordable." },
                    { author: "Preeti Singh", rating: 4, text: "Excellent for engineering at government rates. Faculty is knowledgeable." }
                ]
            },
            {
                name: "Arya College of Engineering & IT",
                minPercentage: 52,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["coding sessions", "workshops", "community"],
                courses: ["B.Tech", "BCA", "M.Tech", "MCA"],
                yearlyPrograms: ["Coding Session", "Workshop Day", "Community Meet"],
                highlights: [
                    "IT focused engineering college",
                    "Modern computer labs",
                    "Regular coding sessions",
                    "Technical workshops",
                    "Active student community"
                ],
                reviews: [
                    { author: "Pankaj Gupta", rating: 3, text: "Good for CSE and IT. Faculty encourages practical learning." },
                    { author: "Anjali Verma", rating: 3, text: "Decent college with focus on programming skills." }
                ]
            },
            {
                name: "Shivalik College of Engineering",
                minPercentage: 53,
                interests: ["Engineering"],
                specificKeywords: ["industrial training", "workshop facilities", "placements"],
                courses: ["B.Tech in CSE", "B.Tech in ME", "B.Tech in Civil", "B.Tech in EE"],
                yearlyPrograms: ["Industrial Training", "Workshop Event", "Placement Fair"],
                highlights: [
                    "Established engineering college",
                    "Focus on practical knowledge",
                    "Regular industrial training",
                    "Good workshop facilities",
                    "Placement assistance"
                ],
                reviews: [
                    { author: "Deepak Mishra", rating: 3, text: "Average engineering college. Faculty is supportive." },
                    { author: "Kavita Sharma", rating: 3, text: "Decent option for engineering education." }
                ]
            },
            {
                name: "Cambridge Institute of Technology",
                minPercentage: 56,
                interests: ["Engineering", "Computer"],
                specificKeywords: ["tech competitions", "collaborations", "placements"],
                courses: ["B.Tech", "M.Tech", "BCA", "MCA"],
                yearlyPrograms: ["Tech Competition", "Collaboration Seminar", "Placement Week"],
                highlights: [
                    "Focus on technical excellence",
                    "Modern infrastructure",
                    "Regular tech competitions",
                    "Industry collaborations",
                    "Active placement cell"
                ],
                reviews: [
                    { author: "Rahul Jain", rating: 3, text: "Good engineering college. Placements are improving." },
                    { author: "Sneha Agarwal", rating: 3, text: "Decent college with good facilities." }
                ]
            },
            {
                name: "Hindustan College of Science & Technology",
                minPercentage: 54,
                interests: ["Engineering", "Science"],
                specificKeywords: ["research opportunities", "science exhibitions", "faculty"],
                courses: ["B.Tech", "B.Sc", "M.Tech", "M.Sc"],
                yearlyPrograms: ["Research Day", "Science Exhibition", "Tech Seminar"],
                highlights: [
                    "Science and technology institute",
                    "Good lab facilities",
                    "Research opportunities",
                    "Experienced faculty",
                    "Regular science exhibitions"
                ],
                reviews: [
                    { author: "Vikas Yadav", rating: 3, text: "Good for engineering and science. Faculty is knowledgeable." },
                    { author: "Nisha Gupta", rating: 3, text: "Decent college with focus on research." }
                ]
            }
        ];

        let allColleges = []; // To store filtered colleges for comparison

        document.getElementById('collegeForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('studentName').value;
            const percentage = parseFloat(document.getElementById('percentage').value);
            const interest = document.getElementById('interest').value;
            const specificInterest = document.getElementById('specificInterest').value.toLowerCase();
            
            // Filter colleges
            let recommendedColleges = colleges.filter(college => {
                const interestMatch = college.interests.includes(interest);
                let specificMatch = true;
                if (specificInterest) {
                    specificMatch = college.specificKeywords.some(keyword => specificInterest.includes(keyword)) ||
                                    college.highlights.some(h => h.toLowerCase().includes(specificInterest)) ||
                                    college.yearlyPrograms.some(p => p.toLowerCase().includes(specificInterest));
                }
                return college.minPercentage <= percentage && interestMatch && specificMatch;
            });
            
            // Sort by match score
            recommendedColleges.sort((a, b) => calculateMatchScore(b, percentage, interest, specificInterest) - calculateMatchScore(a, percentage, interest, specificInterest));
            
            allColleges = recommendedColleges; // For comparison
            
            displayResults(name, recommendedColleges, percentage, interest, specificInterest);
        });

        function displayResults(name, recommendedColleges, percentage, interest, specificInterest) {
            const resultsDiv = document.getElementById('results');
            
            if (recommendedColleges.length === 0) {
                resultsDiv.innerHTML = `
                    <h2>Hello ${name}!</h2>
                    <p style="font-size: 1.2em; color: #666; margin: 20px 0;">
                        Unfortunately, we couldn't find colleges matching your criteria with ${percentage}% in ${interest}. 
                        Please try adjusting your search or consider improving your percentage for better options.
                    </p>
                `;
                resultsDiv.style.display = 'block';
                resultsDiv.scrollIntoView({ behavior: 'smooth' });
                return;
            }
            
            let html = `
                <h2 style="color: #667eea; font-size: 2em; margin-bottom: 20px;">
                    Perfect Matches for ${name}! 🎯
                </h2>
                <p style="font-size: 1.2em; color: #666; margin-bottom: 30px;">
                    Based on your ${percentage}% score and interest in ${interest}${specificInterest ? `, with focus on ${specificInterest}` : ''}, here are the best colleges for you:
                </p>
                
                <div class="best-selects">
                    <h3>🏆 Best Selects for You</h3>
                    <ul id="bestList">
                        ${recommendedColleges.slice(0, 3).map(college => `<li>${college.name}</li>`).join('')}
                    </ul>
                </div>
                
                <button type="button" class="compare-btn" onclick="openComparisonModal()">Compare Selected Colleges</button>
            `;
            
            recommendedColleges.forEach((college, index) => {
                const matchScore = calculateMatchScore(college, percentage, interest, specificInterest);
                html += `
                    <div class="college-card">
                        <input type="checkbox" class="college-checkbox" value="${college.name}" onchange="toggleComparison('${college.name}')">
                        ${index < 3 ? '<div class="recommended-badge">🏆 Top Recommendation</div>' : ''}
                        <div class="college-name">${college.name}</div>
                        
                        <div class="college-info">
                            <div class="info-item">
                                <span class="info-label">Minimum Required:</span> ${college.minPercentage}% (You have ${percentage}%)
                            </div>
                            <div class="info-item">
                                <span class="info-label">Match Score:</span> ${matchScore}%
                            </div>
                        </div>
                        
                        <div class="courses-section">
                            <h3 style="color: #333; margin-bottom: 15px;">📚 Available Courses</h3>
                            ${college.courses.map(course => `<span class="course-tag">${course}</span>`).join('')}
                        </div>
                        
                        <div class="yearly-programs-section">
                            <h3 style="color: #333; margin-bottom: 15px;">📅 Yearly Programs</h3>
                            ${college.yearlyPrograms.map(program => `<span class="course-tag">${program}</span>`).join('')}
                        </div>
                        
                        <div class="highlights">
                            <h3 style="color: #333; margin-bottom: 15px;">✨ Why Choose This College?</h3>
                            ${college.highlights.map(highlight => `<div class="highlight-item">${highlight}</div>`).join('')}
                        </div>
                        
                        <div class="reviews-section">
                            <h3 style="color: #333; margin-bottom: 15px;">💬 Student Reviews</h3>
                            ${college.reviews.map(review => `
                                <div class="review">
                                    <div class="review-author">${review.author}</div>
                                    <div class="star-rating">${'★'.repeat(review.rating)}${'☆'.repeat(5-review.rating)}</div>
                                    <div>${review.text}</div>
                                </div>
                            `).join('')}
                        </div>
                    </div>
                `;
            });
            
            resultsDiv.innerHTML = html;
            resultsDiv.style.display = 'block';
            resultsDiv.scrollIntoView({ behavior: 'smooth' });
        }

        function calculateMatchScore(college, percentage, interest, specificInterest) {
            let score = 0;
            score += 40;
            const excess = percentage - college.minPercentage;
            if (excess > 20) score += 30;
            else if (excess > 10) score += 20;
            else if (excess > 5) score += 10;
            else score += 5;
            if (college.interests.includes(interest)) score += 20;
            const avgRating = college.reviews.reduce((acc, r) => acc + r.rating, 0) / college.reviews.length;
            score += Math.floor(avgRating * 2);
            
            // Specific interest bonus
            if (specificInterest) {
                const matches = college.specificKeywords.filter(k => specificInterest.includes(k.toLowerCase())).length +
                                college.highlights.filter(h => h.toLowerCase().includes(specificInterest)).length +
                                college.yearlyPrograms.filter(p => p.toLowerCase().includes(specificInterest)).length;
                score += matches * 5;
            }
            
            return Math.min(score, 100);
        }

        let selectedColleges = [];

        function toggleComparison(collegeName) {
            const index = selectedColleges.indexOf(collegeName);
            if (index > -1) {
                selectedColleges.splice(index, 1);
            } else {
                selectedColleges.push(collegeName);
            }
        }

        function openComparisonModal() {
            if (selectedColleges.length < 2) {
                alert('Please select at least 2 colleges to compare.');
                return;
            }

            const modal = document.getElementById('compareModal');
            const tableDiv = document.getElementById('comparisonTable');
            let tableHtml = '<table><tr><th>Feature</th>';
            selectedColleges.forEach(collegeName => {
                const college = allColleges.find(c => c.name === collegeName);
                tableHtml += `<th>${collegeName}</th>`;
            });
            tableHtml += '</tr>';

            // Compare courses
            tableHtml += '<tr><td>Courses</td>';
            selectedColleges.forEach(collegeName => {
                const college = allColleges.find(c => c.name === collegeName);
                tableHtml += `<td>${college.courses.join(', ')}</td>`;
            });
            tableHtml += '</tr>';

            // Compare highlights
            tableHtml += '<tr><td>Highlights</td>';
            selectedColleges.forEach(collegeName => {
                const college = allColleges.find(c => c.name === collegeName);
                tableHtml += `<td>${college.highlights.slice(0,3).join('<br>')}</td>`;
            });
            tableHtml += '</tr>';

            // Compare yearly programs
            tableHtml += '<tr><td>Yearly Programs</td>';
            selectedColleges.forEach(collegeName => {
                const college = allColleges.find(c => c.name === collegeName);
                tableHtml += `<td>${college.yearlyPrograms.join(', ')}</td>`;
            });
            tableHtml += '</tr>';

            // Compare avg rating
            tableHtml += '<tr><td>Avg Rating</td>';
            selectedColleges.forEach(collegeName => {
                const college = allColleges.find(c => c.name === collegeName);
                const avg = college.reviews.reduce((acc, r) => acc + r.rating, 0) / college.reviews.length;
                tableHtml += `<td>${avg.toFixed(1)}</td>`;
            });
            tableHtml += '</tr></table>';

            tableDiv.innerHTML = tableHtml;
            modal.style.display = 'block';
        }

        // Modal close
        window.addEventListener('load', function() {
            const closeBtn = document.querySelector('.close');
            if (closeBtn) {
                closeBtn.onclick = function() {
                    document.getElementById('compareModal').style.display = 'none';
                }
            }
        });

        window.onclick = function(event) {
            const modal = document.getElementById('compareModal');
            if (event.target == modal) {
                modal.style.display = 'none';
            }
        }
    </script>
</body>
</html>
