<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>জনদর্পণ (Jonodorpon) - জনগণের আয়নায় সত্যের প্রতিফলন</title>
    <!-- Tailwind CSS for Responsive Design -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brandRed: '#D90429',
                        brandNavy: '#0D1B2A',
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap');
        body { font-family: 'Hind Siliguri', sans-serif; }
    </style>
</head>
<body class="bg-gray-100 text-gray-800 dark:bg-gray-900 dark:text-gray-100 transition-colors duration-300">

    <!-- Top Breaking News Bar -->
    <div class="bg-brandRed text-white text-sm py-2 px-4 flex items-center overflow-hidden">
        <span class="font-bold bg-black px-2 py-1 text-xs rounded uppercase mr-3 shrink-0">ব্রেকিং নিউজ</span>
        <marquee class="font-semibold" behavior="scroll" direction="left">
            জনদর্পণ আপডেট: প্রশাসনিক সিদ্ধান্তের নতুন পর্যবেক্ষণ প্রকাশিত হতে যাচ্ছে আজ রাত ৭টায়... জনস্বার্থ সংক্রান্ত খবরে নিরপেক্ষ চোখ রাখুন আমাদের সাথে!
        </marquee>
    </div>

    <!-- Header / Navbar -->
    <header class="bg-brandNavy text-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <!-- Brand Logo / Name -->
            <div class="flex items-center space-x-3">
                <div class="w-10 h-10 bg-brandRed rounded-full flex items-center justify-center font-bold text-xl border-2 border-white">
                    জ
                </div>
                <div>
                    <h1 class="text-2xl font-bold tracking-wide">জনদর্পণ</h1>
                    <p class="text-xs text-gray-300">Jonodorpon | সত্যের প্রতিফলন</p>
                </div>
            </div>

            <!-- Navigation Links -->
            <nav class="hidden md:flex space-x-6 font-semibold">
                <a href="#" onclick="filterNews('all')" class="hover:text-brandRed transition">সব খবর</a>
                <a href="#" onclick="filterNews('national')" class="hover:text-brandRed transition">জাতীয়</a>
                <a href="#" onclick="filterNews('politics')" class="hover:text-brandRed transition">রাজনীতি</a>
                <a href="#" onclick="filterNews('economy')" class="hover:text-brandRed transition">অর্থনীতি</a>
                <a href="#" onclick="filterNews('analysis')" class="hover:text-brandRed transition">বিশেষ বিশ্লেষণ</a>
            </nav>

            <!-- Right Controls: Dark Mode Toggle -->
            <div class="flex items-center space-x-4">
                <button id="themeToggle" class="p-2 bg-gray-800 dark:bg-gray-700 rounded-full text-yellow-400 focus:outline-none">
                    🌙 Mode
                </button>
            </div>
        </div>
    </header>

    <!-- Main Content Area -->
    <main class="container mx-auto px-4 py-8">

        <!-- Search Bar -->
        <div class="mb-8 max-w-xl mx-auto">
            <input type="text" id="searchInput" onkeyup="searchNews()" placeholder="খবর খুঁজুন (যেমন: পেট্রোল, বিদ্যুৎ, নীতি)..." 
                   class="w-full p-3 rounded-lg border border-gray-300 dark:border-gray-700 dark:bg-gray-800 focus:ring-2 focus:ring-brandRed outline-none shadow-sm">
        </div>

        <!-- Featured / Main Grid -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8" id="newsGrid">
            
            <!-- Card 1 -->
            <div class="news-card bg-white dark:bg-gray-800 rounded-lg shadow-lg overflow-hidden border dark:border-gray-700" data-category="economy">
                <div class="h-48 bg-gray-300 dark:bg-gray-700 relative flex items-center justify-center text-gray-500 font-bold">
                    <span class="absolute top-2 left-2 bg-brandRed text-white text-xs px-2 py-1 rounded">অর্থনীতি</span>
                    [ফটো ব্যানার: সরকারি চুক্তি বিশ্লেষণ]
                </div>
                <div class="p-5">
                    <h2 class="news-title text-xl font-bold mb-2 hover:text-brandRed cursor-pointer">নতুন অর্থনৈতিক নীতিমালা: কার সুবিধা, কার ক্ষতি?</h2>
                    <p class="text-sm text-gray-600 dark:text-gray-300 mb-4">সাম্প্রতিক জারিকৃত নোটিশে সাধারণ মানুষের ক্রয়ক্ষমতায় কী প্রভাব পড়বে? জনদর্পণের বিশেষ পর্যালোচনা।</p>
                    <div class="flex justify-between items-center text-xs text-gray-400">
                        <span>তারিখ: ২১ সেপ্টেম্বর, ২০২৬</span>
                        <button onclick="openModal('নতুন অর্থনৈতিক নীতিমালা', 'এই নীতিমালার বিস্তারিত বিশ্লেষণ খুব শীঘ্রই আপডেট করা হচ্ছে। জনদর্পণের সাথে থাকুন।')" class="text-brandRed font-semibold hover:underline">বিস্তারিত পড়ুন →</button>
                    </div>
                </div>
            </div>

            <!-- Card 2 -->
            <div class="news-card bg-white dark:bg-gray-800 rounded-lg shadow-lg overflow-hidden border dark:border-gray-700" data-category="national">
                <div class="h-48 bg-gray-300 dark:bg-gray-700 relative flex items-center justify-center text-gray-500 font-bold">
                    <span class="absolute top-2 left-2 bg-brandRed text-white text-xs px-2 py-1 rounded">জাতীয়</span>
                    [ফটো ব্যানার: জনস্বার্থ সিদ্ধান্ত]
                </div>
                <div class="p-5">
                    <h2 class="news-title text-xl font-bold mb-2 hover:text-brandRed cursor-pointer">জ্বালানি খাতের ভর্তুকি প্রত্যাহার: নতুন চ্যালেঞ্জে সাধারণ জনগণ</h2>
                    <p class="text-sm text-gray-600 dark:text-gray-300 mb-4">ভর্তুকি কমানোর সিদ্ধান্ত কতটা যৌক্তিক? সরকারি সিদ্ধান্ত ও বাস্তবতার মুখোমুখি পর্যালোচনা।</p>
                    <div class="flex justify-between items-center text-xs text-gray-400">
                        <span>তারিখ: ২০ সেপ্টেম্বর, ২০২৬</span>
                        <button onclick="openModal('জ্বালানি খাতের ভর্তুকি', 'জ্বালানি মূল্যের এই পরিবর্তনের ফলে বাজারে নিত্যপ্রয়োজনীয় পণ্যের দাম বৃদ্ধি পাওয়ার শঙ্কা রয়েছে।')" class="text-brandRed font-semibold hover:underline">বিস্তারিত পড়ুন →</button>
                    </div>
                </div>
            </div>

            <!-- Card 3 -->
            <div class="news-card bg-white dark:bg-gray-800 rounded-lg shadow-lg overflow-hidden border dark:border-gray-700" data-category="analysis">
                <div class="h-48 bg-gray-300 dark:bg-gray-700 relative flex items-center justify-center text-gray-500 font-bold">
                    <span class="absolute top-2 left-2 bg-brandRed text-white text-xs px-2 py-1 rounded">বিশেষ বিশ্লেষণ</span>
                    [ফটো ব্যানার: শিক্ষা কারিকুলাম]
                </div>
                <div class="p-5">
                    <h2 class="news-title text-xl font-bold mb-2 hover:text-brandRed cursor-pointer">শিক্ষা ব্যবস্থার নতুন সংস্কার: শিক্ষক ও শিক্ষার্থীদের মূল্যায়ন</h2>
                    <p class="text-sm text-gray-600 dark:text-gray-300 mb-4">শিক্ষানীতির নতুন প্রয়োগ কতটা কার্যকর হচ্ছে? সরজমিনে জনদর্পণের সরেজমিন রিপোর্ট।</p>
                    <div class="flex justify-between items-center text-xs text-gray-400">
                        <span>তারিখ: ১৯ সেপ্টেম্বর, ২০২৬</span>
                        <button onclick="openModal('শিক্ষা ব্যবস্থার নতুন সংস্কার', 'বিভিন্ন স্কুলের শিক্ষক ও অভিভাবকদের সাথে কথা বলে পাওয়া তথ্যের ভিত্তিতে এই রিপোর্ট তৈরি।')" class="text-brandRed font-semibold hover:underline">বিস্তারিত পড়ুন →</button>
                    </div>
                </div>
            </div>

        </div>

        <!-- Interactive Comments & Feedback Section -->
        <section class="mt-12 bg-white dark:bg-gray-800 p-6 rounded-lg shadow-md border dark:border-gray-700">
            <h3 class="text-2xl font-bold mb-4">জনমত / পাঠকের মন্তব্য (Interactive Discussion)</h3>
            <div id="commentBox" class="space-y-4 mb-6">
                <div class="p-3 bg-gray-100 dark:bg-gray-700 rounded-lg">
                    <span class="font-bold text-sm text-brandRed">পাঠক ১:</span>
                    <p class="text-sm">খবরগুলোর নিরপেক্ষ বিশ্লেষণ বেশ তথ্যবহুল। আশা করি এই ধারাবাহিকতা বজায় থাকবে।</p>
                </div>
            </div>

            <!-- Add Comment Form -->
            <div class="flex gap-2">
                <input type="text" id="userComment" placeholder="আপনার নিরপেক্ষ মতামত লিখুন..." class="flex-1 p-3 border rounded-lg dark:bg-gray-900 dark:border-gray-600 outline-none">
                <button onclick="addComment()" class="bg-brandRed text-white px-6 py-3 rounded-lg font-bold hover:bg-red-700 transition">মন্তব্য দিন</button>
            </div>
        </section>

    </main>

    <!-- Modal Pop-up for Article Reading -->
    <div id="newsModal" class="fixed inset-0 bg-black bg-opacity-50 hidden justify-center items-center p-4 z-50">
        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg max-w-lg w-full relative">
            <button onclick="closeModal()" class="absolute top-3 right-3 text-gray-500 hover:text-black dark:hover:text-white font-bold text-xl">&times;</button>
            <h3 id="modalTitle" class="text-2xl font-bold mb-3"></h3>
            <p id="modalBody" class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed mb-4"></p>
            <button onclick="closeModal()" class="bg-brandNavy text-white px-4 py-2 rounded font-semibold text-sm">বন্ধ করুন</button>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-brandNavy text-white py-6 mt-12 text-center text-sm">
        <p>&copy; ২০২৬ জনদর্পণ (Jonodorpon)। সর্বস্বত্ব সংরক্ষিত।</p>
        <p class="text-gray-400 text-xs mt-1">জনগণের আয়নায় সত্যের প্রতিফলন | স্বাধীন নিউজ ও এনালাইসিস প্ল্যাটফর্ম</p>
    </footer>

    <!-- JavaScript Functionality -->
    <script>
        // Dark Mode Toggle Logic
        const themeToggle = document.getElementById('themeToggle');
        themeToggle.addEventListener('click', () => {
            document.documentElement.classList.toggle('dark');
        });

        // Search Filter Logic
        function searchNews() {
            let input = document.getElementById('searchInput').value.toLowerCase();
            let cards = document.getElementsByClassName('news-card');

            for (let i = 0; i < cards.length; i++) {
                let title = cards[i].querySelector('.news-title').innerText.toLowerCase();
                if (title.includes(input)) {
                    cards[i].style.display = "block";
                } else {
                    cards[i].style.display = "none";
                }
            }
        }

        // Category Filter Logic
        function filterNews(category) {
            let cards = document.getElementsByClassName('news-card');
            for (let i = 0; i < cards.length; i++) {
                if (category === 'all' || cards[i].getAttribute('data-category') === category) {
                    cards[i].style.display = "block";
                } else {
                    cards[i].style.display = "none";
                }
            }
        }

        // Interactive Comment Logic
        function addComment() {
            let input = document.getElementById('userComment');
            let text = input.value.trim();
            if (text !== "") {
                let box = document.getElementById('commentBox');
                let newComment = document.createElement('div');
                newComment.className = "p-3 bg-gray-100 dark:bg-gray-700 rounded-lg";
                newComment.innerHTML = `<span class="font-bold text-sm text-brandRed">আপনি:</span><p class="text-sm">${text}</p>`;
                box.appendChild(newComment);
                input.value = "";
            }
        }

        // Modal Logic
        function openModal(title, content) {
            document.getElementById('modalTitle').innerText = title;
            document.getElementById('modalBody').innerText = content;
            document.getElementById('newsModal').classList.remove('hidden');
            document.getElementById('newsModal').classList.add('flex');
        }

        function closeModal() {
            document.getElementById('newsModal').classList.add('hidden');
            document.getElementById('newsModal').classList.remove('flex');
        }
    </script>
</body>
</html>

