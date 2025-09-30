<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fashion Rental - เช่าเสื้อผ้าแฟชั่นออนไลน์</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            box-sizing: border-box;
            font-family: 'Sarabun', sans-serif; /* แนะนำให้ใช้ Font ที่รองรับภาษาไทย */
        }
        .gradient-bg {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        .card-hover {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
        }
        .fade-in {
            animation: fadeIn 0.6s ease-in;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@400;700&display=swap" rel="stylesheet">
</head>
<body class="bg-gray-50">
    <header class="bg-white shadow-lg sticky top-0 z-50">
        <div class="container mx-auto px-4 py-4">
            <div class="flex items-center justify-between">
                <div class="flex items-center space-x-2">
                    <div class="w-10 h-10 gradient-bg rounded-full flex items-center justify-center">
                        <span class="text-white font-bold text-lg">FR</span>
                    </div>
                    <h1 class="text-2xl font-bold text-gray-800">Fashion Rental</h1>
                </div>
                <nav class="hidden md:flex space-x-8">
                    <a href="#" class="text-gray-600 hover:text-purple-600 transition-colors">หน้าแรก</a>
                    <a href="#" class="text-gray-600 hover:text-purple-600 transition-colors">เสื้อผ้าผู้หญิง</a>
                    <a href="#" class="text-gray-600 hover:text-purple-600 transition-colors">เสื้อผ้าผู้ชาย</a>
                    <a href="#" class="text-gray-600 hover:text-purple-600 transition-colors">อุปกรณ์เสริม</a>
                </nav>
                <div class="flex items-center space-x-4">
                    <button class="p-2 text-gray-600 hover:text-purple-600 transition-colors">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                        </svg>
                    </button>
                    <button id="cartButton" class="p-2 text-gray-600 hover:text-purple-600 transition-colors relative">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                             <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L4.5 18M7 13h10m0 0l-2.5 5m-4.5-5v6a2 2 0 01-2 2H9a2 2 0 01-2-2v-6m8 0V9a2 2 0 00-2-2H9a2 2 0 00-2 2v4.01" />
                        </svg>
                        <span id="cartCounter" class="absolute -top-2 -right-2 bg-purple-600 text-white text-xs rounded-full w-5 h-5 flex items-center justify-center">0</span>
                    </button>
                    <div class="relative">
                        <button id="userButton" class="bg-purple-600 text-white px-4 py-2 rounded-lg hover:bg-purple-700 transition-colors">เข้าสู่ระบบ</button>
                         <div id="userDropdown" class="hidden absolute right-0 mt-2 w-48 bg-white rounded-md shadow-lg py-1 z-50">
                            <a href="#" id="editProfileLink" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">แก้ไขโปรไฟล์</a>
                            <a href="#" id="orderHistoryLink" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">ประวัติการเช่า</a>
                            <a href="#" id="logoutButton" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">ออกจากระบบ</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <section class="gradient-bg text-white py-20">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-5xl font-bold mb-6 fade-in">เช่าแฟชั่นสุดชิค<br>ในราคาที่คุณรักได้</h2>
            <p class="text-xl mb-8 opacity-90 fade-in">เสื้อผ้าแบรนด์เนมคุณภาพสูง เช่าง่าย คืนสะดวก ราคาเริ่มต้นเพียง 299 บาท</p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center fade-in">
                <button class="bg-white text-purple-600 px-8 py-3 rounded-lg font-semibold hover:bg-gray-100 transition-colors">เริ่มเช่าเลย</button>
                <button class="border-2 border-white text-white px-8 py-3 rounded-lg font-semibold hover:bg-white hover:text-purple-600 transition-colors">ดูวิธีการเช่า</button>
            </div>
        </div>
    </section>

    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h3 class="text-3xl font-bold text-center mb-12 text-gray-800">หมวดหมู่เสื้อผ้า</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                <div class="text-center card-hover cursor-pointer">
                    <div class="w-32 h-32 mx-auto mb-4 bg-gradient-to-br from-pink-400 to-purple-600 rounded-full flex items-center justify-center">
                        <span class="text-6xl">👗</span>
                    </div>
                    <h4 class="text-xl font-semibold mb-2">เสื้อผ้าผู้หญิง</h4>
                    <p class="text-gray-600">ชุดราตรี ชุดทำงาน ชุดลำลอง เดรส</p>
                </div>
                <div class="text-center card-hover cursor-pointer">
                    <div class="w-32 h-32 mx-auto mb-4 bg-gradient-to-br from-blue-400 to-indigo-600 rounded-full flex items-center justify-center">
                        <span class="text-6xl">👔</span>
                    </div>
                    <h4 class="text-xl font-semibold mb-2">เสื้อผ้าผู้ชาย</h4>
                    <p class="text-gray-600">สูท เสื้อเชิ้ต เสื้อโปโล เสื้อแจ็คเก็ต</p>
                </div>
            </div>
        </div>
    </section>

    <section class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <h3 class="text-3xl font-bold text-center mb-12 text-gray-800">สินค้าแนะนำ</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-64 bg-gradient-to-br from-pink-200 to-purple-300 flex items-center justify-center">
                        <span class="text-6xl">👗</span>
                    </div>
                    <div class="p-6">
                        <h4 class="font-semibold text-lg mb-2 product-name">ชุดราตรีสีดำ</h4>
                        <p class="text-gray-600 text-sm mb-3">แบรนด์ Zara • ไซส์ S-M</p>
                        <div class="flex items-center justify-between">
                            <div>
                                <span class="text-2xl font-bold text-purple-600 product-price">฿599</span>
                                <span class="text-sm text-gray-500">/3 วัน</span>
                            </div>
                            <button class="rent-button bg-purple-600 text-white px-4 py-2 rounded-lg hover:bg-purple-700 transition-colors">เช่า</button>
                        </div>
                    </div>
                </div>

                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-64 bg-gradient-to-br from-blue-200 to-indigo-300 flex items-center justify-center">
                        <span class="text-6xl">👔</span>
                    </div>
                    <div class="p-6">
                        <h4 class="font-semibold text-lg mb-2 product-name">สูทสีน้ำเงิน</h4>
                        <p class="text-gray-600 text-sm mb-3">แบรนด์ Hugo Boss • ไซส์ M-L</p>
                        <div class="flex items-center justify-between">
                            <div>
                                <span class="text-2xl font-bold text-purple-600 product-price">฿899</span>
                                <span class="text-sm text-gray-500">/3 วัน</span>
                            </div>
                            <button class="rent-button bg-purple-600 text-white px-4 py-2 rounded-lg hover:bg-purple-700 transition-colors">เช่า</button>
                        </div>
                    </div>
                </div>

                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-64 bg-gradient-to-br from-green-200 to-teal-300 flex items-center justify-center">
                        <span class="text-6xl">👕</span>
                    </div>
                    <div class="p-6">
                        <h4 class="font-semibold text-lg mb-2 product-name">เสื้อเชิ้ตขาว</h4>
                        <p class="text-gray-600 text-sm mb-3">แบรนด์ Uniqlo • ไซส์ M-L</p>
                        <div class="flex items-center justify-between">
                            <div>
                                <span class="text-2xl font-bold text-purple-600 product-price">฿299</span>
                                <span class="text-sm text-gray-500">/3 วัน</span>
                            </div>
                            <button class="rent-button bg-purple-600 text-white px-4 py-2 rounded-lg hover:bg-purple-700 transition-colors">เช่า</button>
                        </div>
                    </div>
                </div>

                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-64 bg-gradient-to-br from-yellow-200 to-orange-300 flex items-center justify-center">
                        <span class="text-6xl">👚</span>
                    </div>
                    <div class="p-6">
                        <h4 class="font-semibold text-lg mb-2 product-name">เสื้อบลาวส์</h4>
                        <p class="text-gray-600 text-sm mb-3">แบรนด์ H&M • ไซส์ S-M</p>
                        <div class="flex items-center justify-between">
                            <div>
                                <span class="text-2xl font-bold text-purple-600 product-price">฿399</span>
                                <span class="text-sm text-gray-500">/3 วัน</span>
                            </div>
                            <button class="rent-button bg-purple-600 text-white px-4 py-2 rounded-lg hover:bg-purple-700 transition-colors">เช่า</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-8 h-8 gradient-bg rounded-full flex items-center justify-center">
                            <span class="text-white font-bold">FR</span>
                        </div>
                        <h4 class="text-xl font-bold">Fashion Rental</h4>
                    </div>
                    <p class="text-gray-400">เช่าแฟชั่นแบรนด์เนมคุณภาพสูงในราคาที่คุ้มค่า</p>
                </div>
                <div>
                    <h5 class="font-semibold mb-4">บริการ</h5>
                    <ul class="space-y-2 text-gray-400">
                        <li><a href="#" class="hover:text-white transition-colors">เช่าเสื้อผ้า</a></li>
                        <li><a href="#" class="hover:text-white transition-colors">วิธีการเช่า</a></li>
                        <li><a href="#" class="hover:text-white transition-colors">ราคา</a></li>
                    </ul>
                </div>
                <div>
                    <h5 class="font-semibold mb-4">ช่วยเหลือ</h5>
                    <ul class="space-y-2 text-gray-400">
                        <li><a href="#" class="hover:text-white transition-colors">คำถามที่พบบ่อย</a></li>
                        <li><a href="#" class="hover:text-white transition-colors">ติดต่อเรา</a></li>
                        <li><a href="#" class="hover:text-white transition-colors">นโยบายการคืนสินค้า</a></li>
                    </ul>
                </div>
                <div>
                    <h5 class="font-semibold mb-4">ติดตามเรา</h5>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.71v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" /></svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd" /></svg>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                           <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.024.06 1.378.06 3.808s-.012 2.784-.06 3.808c-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.024.048-1.378.06-3.808.06s-2.784-.012-3.808-.06c-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.048-1.024-.06-1.378-.06-3.808s.012-2.784.06-3.808c.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 016.345 2.525c.636-.247 1.363-.416 2.427-.465C9.793 2.013 10.147 2 12.315 2zM12 4.195c-2.404 0-2.715.01-3.66.056-1.115.053-1.63.228-2.004.382a2.898 2.898 0 00-1.05 1.05c-.154.374-.33.89-.382 2.004-.046.945-.056 1.256-.056 3.66s.01 2.715.056 3.66c.053 1.115.228 1.63.382 2.004a2.898 2.898 0 001.05 1.05c.374.154.89.33 2.004.382.945.046 1.256.056 3.66.056s2.715-.01 3.66-.056c1.115-.053 1.63-.228 2.004-.382a2.898 2.898 0 001.05-1.05c.154-.374.33-.89.382-2.004.046-.945.056-1.256.056-3.66s-.01-2.715-.056-3.66c-.053-1.115-.228-1.63-.382-2.004a2.898 2.898 0 00-1.05-1.05c-.374-.154-.89-.33-2.004-.382C14.715 4.205 14.404 4.195 12 4.195zM12 9.077a2.923 2.923 0 100 5.846 2.923 2.923 0 000-5.846zM12 16a4 4 0 110-8 4 4 0 010 8z" clip-rule="evenodd" /></svg>
                        </a>
                    </div>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400">
                <p>&copy; 2025 Fashion Rental. สงวนลิขสิทธิ์ทุกประการ</p>
            </div>
        </div>
    </footer>

    <div id="loginModal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center p-4">
        <div class="bg-white rounded-xl p-8 max-w-md w-full">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-2xl font-bold text-gray-800">เข้าสู่ระบบ</h3>
                <button id="closeLogin" class="text-gray-500 hover:text-gray-700">&times;</button>
            </div>
            <form id="loginForm">
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2">อีเมล</label>
                    <input type="email" id="loginEmail" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" required>
                </div>
                <div class="mb-6">
                    <label class="block text-gray-700 text-sm font-bold mb-2">รหัสผ่าน</label>
                    <input type="password" id="loginPassword" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" required>
                </div>
                <button type="submit" class="w-full bg-purple-600 text-white py-2 rounded-lg hover:bg-purple-700 transition-colors">เข้าสู่ระบบ</button>
                <p class="text-center text-gray-600 mt-4">ยังไม่มีบัญชี? <a href="#" id="showRegister" class="text-purple-600 hover:underline">สมัครสมาชิก</a></p>
            </form>
        </div>
    </div>

    <div id="registerModal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center p-4">
        <div class="bg-white rounded-xl p-8 max-w-md w-full">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-2xl font-bold text-gray-800">สมัครสมาชิก</h3>
                <button id="closeRegister" class="text-gray-500 hover:text-gray-700">&times;</button>
            </div>
            <form id="registerForm">
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2">ชื่อ-นามสกุล</label>
                    <input type="text" id="registerName" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" required>
                </div>
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2">อีเมล</label>
                    <input type="email" id="registerEmail" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" required>
                </div>
                <div class="mb-6">
                    <label class="block text-gray-700 text-sm font-bold mb-2">รหัสผ่าน</label>
                    <input type="password" id="registerPassword" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" required>
                </div>
                <button type="submit" class="w-full bg-purple-600 text-white py-2 rounded-lg hover:bg-purple-700 transition-colors">สมัครสมาชิก</button>
                <p class="text-center text-gray-600 mt-4">มีบัญชีแล้ว? <a href="#" id="showLogin" class="text-purple-600 hover:underline">เข้าสู่ระบบ</a></p>
            </form>
        </div>
    </div>

    <div id="editProfileModal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center p-4">
        <div class="bg-white rounded-xl p-8 max-w-md w-full">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-2xl font-bold text-gray-800">แก้ไขโปรไฟล์</h3>
                <button id="closeEditProfile" class="text-gray-500 hover:text-gray-700">&times;</button>
            </div>
            <form id="editProfileForm">
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2">ชื่อ-นามสกุล</label>
                    <input type="text" id="editName" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" required>
                </div>
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2">อีเมล</label>
                    <input type="email" id="editEmail" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" required>
                </div>
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2">เบอร์โทรศัพท์</label>
                    <input type="tel" id="editPhone" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" placeholder="08X-XXX-XXXX">
                </div>
                <div class="mb-6">
                    <label class="block text-gray-700 text-sm font-bold mb-2">ที่อยู่</label>
                    <textarea id="editAddress" rows="3" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600" placeholder="ที่อยู่สำหรับจัดส่ง"></textarea>
                </div>
                <button type="submit" class="w-full bg-purple-600 text-white py-2 rounded-lg hover:bg-purple-700 transition-colors">บันทึกการเปลี่ยนแปลง</button>
            </form>
        </div>
    </div>

    <div id="orderHistoryModal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center p-4">
        <div class="bg-white rounded-xl p-8 max-w-2xl w-full max-h-[90vh] overflow-y-auto">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-2xl font-bold text-gray-800">ประวัติการเช่า</h3>
                <button id="closeOrderHistory" class="text-gray-500 hover:text-gray-700">&times;</button>
            </div>
            <div id="orderHistoryContent">
                <div class="space-y-4">
                    <div class="border rounded-lg p-4">
                        <div class="flex justify-between items-start mb-2">
                            <div>
                                <h4 class="font-semibold">คำสั่งเช่า #001</h4>
                                <p class="text-sm text-gray-600">วันที่: 15 ก.ย. 2025</p>
                            </div>
                            <span class="bg-green-100 text-green-800 px-2 py-1 rounded-full text-xs font-medium">เสร็จสิ้น</span>
                        </div>
                        <div class="text-sm">
                            <p>• ชุดราตรีสีดำ - ฿599</p>
                            <p class="font-semibold mt-2">รวม: ฿599</p>
                        </div>
                    </div>
                    <div class="border rounded-lg p-4">
                        <div class="flex justify-between items-start mb-2">
                            <div>
                                <h4 class="font-semibold">คำสั่งเช่า #002</h4>
                                <p class="text-sm text-gray-600">วันที่: 10 ก.ย. 2025</p>
                            </div>
                            <span class="bg-blue-100 text-blue-800 px-2 py-1 rounded-full text-xs font-medium">กำลังเช่า</span>
                        </div>
                        <div class="text-sm">
                            <p>• สูทสีน้ำเงิน - ฿899</p>
                            <p class="font-semibold mt-2">รวม: ฿899</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
   
    <div id="paymentModal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center p-4">
        <div class="bg-white rounded-xl p-8 max-w-lg w-full">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-2xl font-bold text-gray-800">ชำระเงิน</h3>
                <button id="closePayment" class="text-gray-500 hover:text-gray-700">&times;</button>
            </div>
            <div id="paymentContent">
                <div class="mb-6 p-4 bg-gray-50 rounded-lg">
                    <h4 class="font-semibold mb-2">รายการสินค้า</h4>
                    <div id="paymentItems" class="space-y-1 text-sm"></div>
                    <div class="border-t pt-2 mt-2">
                        <div class="flex justify-between font-bold">
                            <span>รวมทั้งหมด:</span>
                            <span id="totalAmount">฿0</span>
                        </div>
                    </div>
                </div>
                <form id="paymentForm">
                    <div class="bg-yellow-100 border-l-4 border-yellow-500 text-yellow-700 p-4 mb-6" role="alert">
                        <p class="font-bold">หน้าตัวอย่าง</p>
                        <p>ระบบชำระเงินนี้เป็นเพียงตัวอย่าง ไม่มีการทำธุรกรรมเกิดขึ้นจริง</p>
                    </div>
                    <button type="submit" class="w-full bg-purple-600 text-white py-3 rounded-lg hover:bg-purple-700 transition-colors font-semibold">ยืนยันการเช่า</button>
                </form>
            </div>
        </div>
    </div>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            let currentUser = null;
            let cart = [];

            // DOM Elements
            const modals = {
                login: document.getElementById('loginModal'),
                register: document.getElementById('registerModal'),
                payment: document.getElementById('paymentModal'),
                editProfile: document.getElementById('editProfileModal'),
                orderHistory: document.getElementById('orderHistoryModal')
            };

            const userButton = document.getElementById('userButton');
            const userDropdown = document.getElementById('userDropdown');
            const cartCounter = document.getElementById('cartCounter');

            // --- Modal Controls ---
            function showModal(modalId) {
                if (modals[modalId]) modals[modalId].classList.remove('hidden');
            }

            function hideModal(modalId) {
                if (modals[modalId]) modals[modalId].classList.add('hidden');
            }

            // Close buttons for all modals
            document.querySelectorAll('[id^="close"]').forEach(button => {
                const modalId = button.id.replace('close', '').toLowerCase();
                button.addEventListener('click', () => hideModal(modalId));
            });

            // Switch between login and register modals
            document.getElementById('showRegister').addEventListener('click', e => {
                e.preventDefault();
                hideModal('login');
                showModal('register');
            });
            document.getElementById('showLogin').addEventListener('click', e => {
                e.preventDefault();
                hideModal('register');
                showModal('login');
            });
           
            // --- User & UI Controls ---
            function updateUserInterface() {
                if (currentUser) {
                    userButton.innerHTML = `
                        <div class="flex items-center space-x-2">
                            <span>สวัสดี, ${currentUser.name}</span>
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                        </div>`;
                } else {
                    userButton.textContent = 'เข้าสู่ระบบ';
                    userDropdown.classList.add('hidden');
                }
            }
           
            userButton.addEventListener('click', () => {
                if (currentUser) {
                    userDropdown.classList.toggle('hidden');
                } else {
                    showModal('login');
                }
            });
           
            // Close dropdown if clicked outside
             document.addEventListener('click', function(event) {
                if (!userButton.contains(event.target) && !userDropdown.contains(event.target)) {
                    userDropdown.classList.add('hidden');
                }
            });


            // --- Form Submissions ---
            document.getElementById('loginForm').addEventListener('submit', function(e) {
                e.preventDefault();
                const email = document.getElementById('loginEmail').value;
                currentUser = { name: email.split('@')[0], email: email, phone: '', address: '' };
                this.reset();
                hideModal('login');
                updateUserInterface();
                alert('เข้าสู่ระบบสำเร็จ!');
            });

            document.getElementById('registerForm').addEventListener('submit', function(e) {
                e.preventDefault();
                const name = document.getElementById('registerName').value;
                const email = document.getElementById('registerEmail').value;
                currentUser = { name: name, email: email, phone: '', address: '' };
                this.reset();
                hideModal('register');
                updateUserInterface();
                alert('สมัครสมาชิกสำเร็จ!');
            });

            document.getElementById('editProfileForm').addEventListener('submit', function(e) {
                e.preventDefault();
                currentUser.name = document.getElementById('editName').value;
                currentUser.email = document.getElementById('editEmail').value;
                currentUser.phone = document.getElementById('editPhone').value;
                currentUser.address = document.getElementById('editAddress').value;
                hideModal('editProfile');
                updateUserInterface();
                alert('บันทึกข้อมูลเรียบร้อยแล้ว!');
            });
           
            document.getElementById('paymentForm').addEventListener('submit', function(e) {
                e.preventDefault();
                hideModal('payment');
                alert(`ขอบคุณสำหรับการเช่า, ${currentUser.name}!\nคำสั่งเช่าของคุณได้รับการยืนยันแล้ว`);
                cart = [];
                updateCartCounter();
            });


            // --- Dropdown Menu Actions ---
            document.getElementById('logoutButton').addEventListener('click', e => {
                e.preventDefault();
                currentUser = null;
                updateUserInterface();
                alert('ออกจากระบบเรียบร้อยแล้ว');
            });
           
            document.getElementById('editProfileLink').addEventListener('click', e => {
                e.preventDefault();
                userDropdown.classList.add('hidden');
                // Pre-fill form
                document.getElementById('editName').value = currentUser.name;
                document.getElementById('editEmail').value = currentUser.email;
                document.getElementById('editPhone').value = currentUser.phone || '';
                document.getElementById('editAddress').value = currentUser.address || '';
                showModal('editProfile');
            });
           
            document.getElementById('orderHistoryLink').addEventListener('click', e => {
                e.preventDefault();
                userDropdown.classList.add('hidden');
                showModal('orderHistory');
            });


            // --- Cart Functionality ---
            function updateCartCounter() {
                cartCounter.textContent = cart.length;
            }

            document.querySelectorAll('.rent-button').forEach(button => {
                button.addEventListener('click', () => {
                    if (!currentUser) {
                        alert('กรุณาเข้าสู่ระบบก่อนทำการเช่าสินค้า');
                        showModal('login');
                        return;
                    }

                    const card = button.closest('.p-6');
                    const name = card.querySelector('.product-name').textContent;
                    const priceText = card.querySelector('.product-price').textContent;
                    const price = parseFloat(priceText.replace('฿', ''));
                   
                    cart.push({ name, price });
                    updateCartCounter();
                    alert(`เพิ่ม '${name}' ลงในตะกร้าแล้ว`);
                });
            });
           
            document.getElementById('cartButton').addEventListener('click', () => {
                if (!currentUser) {
                    alert('กรุณาเข้าสู่ระบบเพื่อดูตะกร้าสินค้า');
                    showModal('login');
                    return;
                }
                if (cart.length === 0) {
                    alert('ตะกร้าสินค้าของคุณว่างอยู่');
                    return;
                }
               
                const paymentItems = document.getElementById('paymentItems');
                const totalAmount = document.getElementById('totalAmount');
                let total = 0;
               
                paymentItems.innerHTML = '';
               
                cart.forEach(item => {
                    const itemElement = document.createElement('div');
                    itemElement.className = 'flex justify-between';
                    itemElement.innerHTML = `<span>${item.name}</span><span>฿${item.price}</span>`;
                    paymentItems.appendChild(itemElement);
                    total += item.price;
                });
               
                totalAmount.textContent = `฿${total}`;
                showModal('payment');
            });

        });
    </script>
</body>
</html>
