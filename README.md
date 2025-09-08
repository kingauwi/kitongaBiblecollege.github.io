# kitongaBiblecollege.github.io
bible college
                                          
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kitonga Bible College - Student Registration</title>
    <script src="https://cdn.jsdelivr.net/npm/react@18.0.0/umd/react.development.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/react-dom@18.0.0/umd/react-dom.development.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@babel/standalone/babel.js"></script>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"></link>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
        }
        .playfair {
            font-family: 'Playfair Display', serif;
        }
    </style>
</head>
<body>
    <div id="root"></div>

    <script type="text/babel">
        const App = () => {
            const [showRegistrationForm, setShowRegistrationForm] = React.useState(false);
            
            return (
                <div className="min-h-screen flex flex-col">
                    {/* Header */}
                    <header className="bg-white shadow-md sticky top-0 z-50">
                        <div className="container mx-auto px-4 py-3 flex items-center justify-between">
                            <div className="flex items-center">
                                <h1 className="text-2xl font-bold text-blue-800 playfair">Kitonga Bible College</h1>
                            </div>
                            
                            <nav className="hidden md:flex space-x-8">
                                <a href="#home" className="text-gray-800 hover:text-blue-600">Home</a>
                                <a href="#about" className="text-gray-800 hover:text-blue-600">About</a>
                                <a href="#courses" className="text-gray-800 hover:text-blue-600">Courses</a>
                                <a href="#faculty" className="text-gray-800 hover:text-blue-600">Faculty</a>
                                <a href="#contact" className="text-gray-800 hover:text-blue-600">Contact</a>
                            </nav>
                            
                            <button 
                                onClick={() => setShowRegistrationForm(true)}
                                className="bg-blue-600 hover:bg-blue-700 text-white font-medium py-2 px-4 rounded-md transition duration-300"
                            >
                                Register Now
                            </button>
                        </div>
                    </header>

                    {/* Hero Section */}
                    <section id="home" className="bg-blue-600 text-white py-16">
                        <div className="container mx-auto px-4 text-center">
                            <h1 className="text-4xl md:text-5xl font-bold mb-4 playfair">Welcome to Kitonga Bible College</h1>
                            <p className="text-xl mb-8 max-w-3xl mx-auto">
                                Empowering future leaders through biblical education and practical training.
                            </p>
                            <button 
                                onClick={() => setShowRegistrationForm(true)}
                                className="bg-white text-blue-600 hover:bg-gray-100 font-semibold py-3 px-8 rounded-md transition duration-300"
                            >
                                Apply Now
                            </button>
                        </div>
                    </section>

                    {/* Registration Form Modal - Full Screen Version */}
                    {showRegistrationForm && (
                        <div className="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
                            <div className="bg-white rounded-lg p-8 w-full max-w-4xl mx-4 overflow-y-auto max-h-screen">
                                <div className="flex justify-between items-center mb-6">
                                    <h2 className="text-2xl font-bold text-blue-800 playfair">Student Registration</h2>
                                    <button 
                                        onClick={() => setShowRegistrationForm(false)}
                                        className="text-gray-500 hover:text-gray-700"
                                    >
                                        <i className="fas fa-times"></i>
                                    </button>
                                </div>
                                
                                <form className="space-y-4">
                                    <div>
                                        <label className="block text-gray-700 mb-2">Full Name</label>
                                        <input 
                                            type="text" 
                                            className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                            required
                                        />
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Date of Birth</label>
                                        <input 
                                            type="date" 
                                            className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                            required
                                        />
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Gender</label>
                                        <select className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                                            <option>Select Gender</option>
                                            <option>Male</option>
                                            <option>Female</option>
                                            <option>Other</option>
                                        </select>
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Address</label>
                                        <textarea 
                                            className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                            rows="3"
                                        ></textarea>
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Phone Number</label>
                                        <input 
                                            type="tel" 
                                            className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                            required
                                        />
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Email Address</label>
                                        <input 
                                            type="email" 
                                            className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                            required
                                        />
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Previous Education</label>
                                        <select className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                                            <option>Select Level</option>
                                            <option>O-Level</option>
                                            <option>A-Level</option>
                                            <option>Diploma</option>
                                            <option>Bachelor's Degree</option>
                                        </select>
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Course of Interest</label>
                                        <select className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
                                            <option>Select Course</option>
                                            <option>Bachelor of Theology</option>
                                            <option>Diploma in Christian Ministry</option>
                                            <option>Certificate in Biblical Studies</option>
                                            <option>Masters in Divinity</option>
                                        </select>
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Emergency Contact Person</label>
                                        <input 
                                            type="text" 
                                            className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                        />
                                    </div>
                                    <div>
                                        <label className="block text-gray-700 mb-2">Emergency Contact Phone</label>
                                        <input 
                                            type="tel" 
                                            className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                        />
                                    </div>
                                    <div className="pt-4">
                                        <button 
                                            type="submit" 
                                            className="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-4 rounded-md transition duration-300"
                                        >
                                            Submit Application
                                        </button>
                                    </div>
                                </form>
                                <div className="mt-4 text-center text-gray-600">
                                    Already have an account? <a href="#" className="text-blue-600 hover:text-blue-800">Log In</a>
                                </div>
                            </div>
                        </div>
                    )}

                    {/* About Section */}
                    <section id="about" className="py-16 bg-gray-50">
                        <div className="container mx-auto px-4">
                            <div className="text-center mb-12">
                                <h2 className="text-3xl font-bold text-blue-800 playfair mb-4">About Kitonga Bible College</h2>
                                <p className="text-gray-600 max-w-3xl mx-auto">
                                    Established in 1995, Kitonga Bible College is committed to providing high-quality theological education that prepares students for ministry and leadership roles within the church and community. Our mission is to equip believers with the knowledge and skills needed to serve effectively in various capacities.
                                </p>
                            </div>
                            
                            <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <div className="text-blue-600 text-4xl mb-4">
                                        <i className="fas fa-graduation-cap"></i>
                                    </div>
                                    <h3 className="text-xl font-semibold mb-3">Academic Excellence</h3>
                                    <p className="text-gray-600">
                                        Our faculty consists of experienced theologians and practitioners who bring both academic rigor and real-world experience to the classroom.
                                    </p>
                                </div>
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <div className="text-blue-600 text-4xl mb-4">
                                        <i className="fas fa-users"></i>
                                    </div>
                                    <h3 className="text-xl font-semibold mb-3">Community Focus</h3>
                                    <p className="text-gray-600">
                                        We believe in learning by doing. Students participate in outreach programs, church planting initiatives, and community service projects throughout their studies.
                                    </p>
                                </div>
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <div className="text-blue-600 text-4xl mb-4">
                                        <i className="fas fa-book-open"></i>
                                    </div>
                                    <h3 className="text-xl font-semibold mb-3">Biblical Foundation</h3>
                                    <p className="text-gray-600">
                                        Every course is grounded in Scripture, helping students develop a deep understanding of God's Word and its application to modern life and ministry.
                                    </p>
                                </div>
                            </div>
                        </div>
                    </section>

                    {/* Courses Section */}
                    <section id="courses" className="py-16">
                        <div className="container mx-auto px-4">
                            <div className="text-center mb-12">
                                <h2 className="text-3xl font-bold text-blue-800 playfair mb-4">Our Academic Programs</h2>
                                <p className="text-gray-600 max-w-3xl mx-auto">
                                    Choose from a variety of programs designed to meet your educational goals and prepare you for effective ministry.
                                </p>
                            </div>
                            
                            <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <div className="text-blue-600 text-3xl mb-4">
                                        <i className="fas fa-church"></i>
                                    </div>
                                    <h3 className="text-xl font-semibold mb-3">Bachelor of Theology</h3>
                                    <p className="text-gray-600 mb-4">
                                        A comprehensive four-year program covering Old Testament, New Testament, systematic theology, pastoral ministry, and more.
                                    </p>
                                    <div className="flex justify-between items-center">
                                        <span className="text-blue-600 font-semibold">Duration: 4 Years</span>
                                        <a href="#" className="text-blue-600 hover:text-blue-800">Learn More →</a>
                                    </div>
                                </div>
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <div className="text-blue-600 text-3xl mb-4">
                                        <i className="fas fa-certificate"></i>
                                    </div>
                                    <h3 className="text-xl font-semibold mb-3">Diploma in Christian Ministry</h3>
                                    <p className="text-gray-600 mb-4">
                                        A two-year intensive program focusing on practical ministry skills, leadership development, and biblical studies.
                                    </p>
                                    <div className="flex justify-between items-center">
                                        <span className="text-blue-600 font-semibold">Duration: 2 Years</span>
                                        <a href="#" className="text-blue-600 hover:text-blue-800">Learn More →</a>
                                    </div>
                                </div>
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <div className="text-blue-600 text-3xl mb-4">
                                        <i className="fas fa-book"></i>
                                    </div>
                                    <h3 className="text-xl font-semibold mb-3">Certificate in Biblical Studies</h3>
                                    <p className="text-gray-600 mb-4">
                                        A one-year foundational program introducing students to key biblical concepts, doctrines, and ministry principles.
                                    </p>
                                    <div className="flex justify-between items-center">
                                        <span className="text-blue-600 font-semibold">Duration: 1 Year</span>
                                        <a href="#" className="text-blue-600 hover:text-blue-800">Learn More →</a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </section>

                    {/* Faculty Section */}
                    <section id="faculty" className="py-16 bg-gray-50">
                        <div className="container mx-auto px-4">
                            <div className="text-center mb-12">
                                <h2 className="text-3xl font-bold text-blue-800 playfair mb-4">Meet Our Faculty</h2>
                                <p className="text-gray-600 max-w-3xl mx-auto">
                                    Our dedicated team of instructors brings a wealth of knowledge and experience to help shape the next generation of Christian leaders.
                                </p>
                            </div>
                            
                            <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <img 
                                        src="https://picsum.photos/seed/faculty1/300/300.jpg" 
                                        alt="Dr. John Mwangi" 
                                        className="w-full h-64 object-cover rounded-lg mb-4"
                                    />
                                    <h3 className="text-xl font-semibold mb-2">Dr. John Mwangi</h3>
                                    <p className="text-blue-600 mb-3">President & Professor of Theology</p>
                                    <p className="text-gray-600 mb-4">
                                        Dr. Mwangi has over 25 years of experience in theological education and church leadership. He holds a PhD in Systematic Theology from Oxford University.
                                    </p>
                                    <div className="flex space-x-3">
                                        <a href="#" className="text-blue-600 hover:text-blue-800">
                                            <i className="fab fa-linkedin"></i>
                                        </a>
                                        <a href="#" className="text-blue-600 hover:text-blue-800">
                                            <i className="fas fa-envelope"></i>
                                        </a>
                                    </div>
                                </div>
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <img 
                                        src="https://picsum.photos/seed/faculty2/300/300.jpg" 
                                        alt="Prof. Sarah Njoroge" 
                                        className="w-full h-64 object-cover rounded-lg mb-4"
                                    />
                                    <h3 className="text-xl font-semibold mb-2">Prof. Sarah Njoroge</h3>
                                    <p className="text-blue-600 mb-3">Dean of Students & Professor of New Testament</p>
                                    <p className="text-gray-600 mb-4">
                                        Prof. Njoroge specializes in Pauline epistles and has authored several books on early Christianity. She has served as a missionary in East Africa for 15 years.
                                    </p>
                                    <div className="flex space-x-3">
                                        <a href="#" className="text-blue-600 hover:text-blue-800">
                                            <i className="fab fa-linkedin"></i>
                                        </a>
                                        <a href="#" className="text-blue-600 hover:text-blue-800">
                                            <i className="fas fa-envelope"></i>
                                        </a>
                                    </div>
                                </div>
                                <div className="bg-white p-6 rounded-lg shadow-md">
                                    <img 
                                        src="https://picsum.photos/seed/faculty3/300/300.jpg" 
                                        alt="Rev. David Ochieng" 
                                        className="w-full h-64 object-cover rounded-lg mb-4"
                                    />
                                    <h3 className="text-xl font-semibold mb-2">Rev. David Ochieng</h3>
                                    <p className="text-blue-600 mb-3">Director of Pastoral Ministries</p>
                                    <p className="text-gray-600 mb-4">
                                        Rev. Ochieng has extensive experience in church planting and pastoral care. He holds an MDiv from Nairobi Evangelical Graduate School of Theology.
                                    </p>
                                    <div className="flex space-x-3">
                                        <a href="#" className="text-blue-600 hover:text-blue-800">
                                            <i className="fab fa-linkedin"></i>
                                        </a>
                                        <a href="#" className="text-blue-600 hover:text-blue-800">
                                            <i className="fas fa-envelope"></i>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </section>

                    {/* Contact Section */}
                    <section id="contact" className="py-16">
                        <div className="container mx-auto px-4">
                            <div className="text-center mb-12">
                                <h2 className="text-3xl font-bold text-blue-800 playfair mb-4">Contact Us</h2>
                                <p className="text-gray-600 max-w-3xl mx-auto">
                                    Have questions about our programs or admissions process? We're here to help!
                                </p>
                            </div>
                            
                            <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
                                <div className="bg-white p-8 rounded-lg shadow-md">
                                    <h3 className="text-xl font-semibold mb-6">Send us a message</h3>
                                    <form className="space-y-4">
                                        <div>
                                            <label className="block text-gray-700 mb-2">Name</label>
                                            <input 
                                                type="text" 
                                                className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                            />
                                        </div>
                                        <div>
                                            <label className="block text-gray-700 mb-2">Email</label>
                                            <input 
                                                type="email" 
                                                className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                            />
                                        </div>
                                        <div>
                                            <label className="block text-gray-700 mb-2">Subject</label>
                                            <input 
                                                type="text" 
                                                className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                            />
                                        </div>
                                        <div>
                                            <label className="block text-gray-700 mb-2">Message</label>
                                            <textarea 
                                                className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                                                rows="5"
                                            ></textarea>
                                        </div>
                                        <div>
                                            <button 
                                                type="submit" 
                                                className="bg-blue-600 hover:bg-blue-700 text-white font-semibold py-2 px-6 rounded-md transition duration-300"
                                            >
                                                Send Message
                                            </button>
                                        </div>
                                    </form>
                                </div>
                                
                                <div className="bg-white p-8 rounded-lg shadow-md">
                                    <h3 className="text-xl font-semibold mb-6">Visit Us</h3>
                                    <div className="space-y-6">
                                        <div className="flex items-start">
                                            <div className="text-blue-600 mr-4">
                                                <i className="fas fa-map-marker-alt text-xl"></i>
                                            </div>
                                            <div>
                                                <h4 className="font-semibold">Location</h4>
                                                <p className="text-gray-600">Kitonga Bible College<br />P.O. Box 45678-00100<br />Nairobi, Kenya</p>
                                            </div>
                                        </div>
                                        
                                        <div className="flex items-start">
                                            <div className="text-blue-600 mr-4">
                                                <i className="fas fa-phone-alt text-xl"></i>
                                            </div>
                                            <div>
                                                <h4 className="font-semibold">Phone</h4>
                                                <p className="text-gray-600">Main Office: +254 20 123 4567<br />Admissions: +254 20 123 4568</p>
                                            </div>
                                        </div>
                                        
                                        <div className="flex items-start">
                                            <div className="text-blue-600 mr-4">
                                                <i className="fas fa-envelope text-xl"></i>
                                            </div>
                                            <div>
                                                <h4 className="font-semibold">Email</h4>
                                                <p className="text-gray-600">info@kitongabiblecollege.ac.ke<br />admissions@kitongabiblecollege.ac.ke</p>
                                            </div>
                                        </div>
                                    </div>
                                    
                                    <div className="mt-8">
                                        <h4 className="font-semibold mb-4">Follow Us</h4>
                                        <div className="flex space-x-4">
                                            <a href="#" className="text-gray-600 hover:text-blue-600 text-xl">
                                                <i className="fab fa-facebook-f"></i>
                                            </a>
                                            <a href="#" className="text-gray-600 hover:text-blue-600 text-xl">
                                                <i className="fab fa-twitter"></i>
                                            </a>
                                            <a href="#" className="text-gray-600 hover:text-blue-600 text-xl">
                                                <i className="fab fa-instagram"></i>
                                            </a>
                                            <a href="#" className="text-gray-600 hover:text-blue-600 text-xl">
                                                <i className="fab fa-youtube"></i>
                                            </a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </section>

                    {/* Footer */}
                    <footer className="bg-gray-900 text-white py-12">
                        <div className="container mx-auto px-4">
                            <div className="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                                <div>
                                    <h3 className="text-xl font-semibold mb-4">Kitonga Bible College</h3>
                                    <p className="text-gray-400 mb-4">
                                        Equipping servant-leaders through biblical education and practical training.
                                    </p>
                                    <div className="flex space-x-4">
                                        <a href="#" className="text-gray-400 hover:text-white">
                                            <i className="fab fa-facebook-f"></i>
                                        </a>
                                        <a href="#" className="text-gray-400 hover:text-white">
                                            <i className="fab fa-twitter"></i>
                                        </a>
                                        <a href="#" className="text-gray-400 hover:text-white">
                                            <i className="fab fa-instagram"></i>
                                        </a>
                                        <a href="#" className="text-gray-400 hover:text-white">
                                            <i className="fab fa-youtube"></i>
                                        </a>
                                    </div>
                                </div>
                                <div>
                                    <h3 className="text-lg font-semibold mb-4">Quick Links</h3>
                                    <ul className="space-y-2">
                                        <li><a href="#" className="text-gray-400 hover:text-white">Home</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">About</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">Courses</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">Faculty</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">Admissions</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">Contact</a></li>
                                    </ul>
                                </div>
                                <div>
                                    <h3 className="text-lg font-semibold mb-4">Resources</h3>
                                    <ul className="space-y-2">
                                        <li><a href="#" className="text-gray-400 hover:text-white">Library</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">Online Courses</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">Study Materials</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">Events Calendar</a></li>
                                        <li><a href="#" className="text-gray-400 hover:text-white">FAQ</a></li>
                                    </ul>
                                </div>
                                <div>
                                    <h3 className="text-lg font-semibold mb-4">Contact Info</h3>
                                    <ul className="space-y-2 text-gray-400">
                                        <li className="flex items-start">
                                            <i className="fas fa-map-marker-alt mt-1 mr-2"></i>
                                            <span>P.O. Box 45678-00100, Nairobi, Kenya</span>
                                        </li>
                                        <li className="flex items-center">
                                            <i className="fas fa-phone-alt mr-2"></i>
                                            <span>+254 7844 66920</span>
                                        </li>
                                        <li className="flex items-center">
                                            <i className="fas fa-envelope mr-2"></i>
                                            <span>info@kitongabiblecollege.ac.ke</span>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                            <div className="border-t border-gray-800 pt-6 text-center text-gray-500 text-sm">
                                © 2023 Kitonga Bible College. All rights reserved.
                            </div>
                        </div>
                    </footer>
                </div>
            );
        };

        ReactDOM.render(<App />, document.getElementById('root'));
    </script>
</body>
</html>




























































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































