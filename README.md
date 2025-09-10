<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لینکدونی | Link VIPZEXNET</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2980b9;
            --accent-color: #e74c3c;
            --light-bg: #f8f9fa;
            --dark-text: #2c3e50;
            --gradient: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Vazir', 'Tanha', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light-bg);
            color: var(--dark-text);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* صفحه ورود و ثبت نام */
        .auth-container {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(rgba(255,255,255,0.9), rgba(255,255,255,0.9)), 
                        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%23f8f9fa"/><path d="M0,0 L100,100" stroke="%233498db" stroke-width="2" opacity="0.2"/><path d="M100,0 L0,100" stroke="%233498db" stroke-width="2" opacity="0.2"/></svg>');
            background-size: 300px;
        }

        .auth-card {
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            width: 100%;
            max-width: 400px;
            overflow: hidden;
        }

        .auth-header {
            background: var(--gradient);
            color: white;
            padding: 20px;
            text-align: center;
        }

        .auth-header h1 {
            font-size: 1.8rem;
            margin-bottom: 5px;
        }

        .auth-header p {
            opacity: 0.9;
        }

        .auth-body {
            padding: 20px;
        }

        .auth-tabs {
            display: flex;
            border-bottom: 1px solid #eee;
            margin-bottom: 20px;
        }

        .auth-tab {
            flex: 1;
            text-align: center;
            padding: 10px;
            cursor: pointer;
            transition: all 0.3s;
            border-bottom: 3px solid transparent;
        }

        .auth-tab.active {
            border-bottom: 3px solid var(--primary-color);
            color: var(--primary-color);
            font-weight: bold;
        }

        .auth-form {
            display: none;
        }

        .auth-form.active {
            display: block;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .form-control:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
        }

        .btn {
            display: block;
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s;
        }

        .btn-primary {
            background: var(--gradient);
            color: white;
        }

        .btn-primary:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        .error-message {
            color: var(--accent-color);
            font-size: 0.85rem;
            margin-top: 5px;
            display: none;
        }

        /* صفحه اصلی */
        .main-app {
            display: none;
            min-height: 100vh;
        }

        .navbar {
            background: var(--gradient);
            color: white;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .navbar-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.5rem;
            font-weight: bold;
        }

        .logo i {
            margin-left: 10px;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin: 0 10px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            padding: 5px 10px;
            border-radius: 5px;
            transition: background 0.3s;
        }

        .nav-links a:hover {
            background: rgba(255,255,255,0.1);
        }

        .main-content {
            padding: 30px 0;
        }

        .section-title {
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--primary-color);
            font-size: 1.5rem;
        }

        /* استایل جدید برای بنرهای کشویی */
        .banners-slider {
            position: relative;
            height: 250px;
            overflow: hidden;
            margin-bottom: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .banner-slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            transition: opacity 1s ease-in-out;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: flex-end;
            padding: 20px;
            color: white;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.7);
        }

        .banner-slide.active {
            opacity: 1;
        }

        .banner-info {
            background: rgba(0,0,0,0.6);
            padding: 15px;
            border-radius: 8px;
            width: 100%;
        }

        .banner-slide-title {
            font-size: 1.4rem;
            margin-bottom: 5px;
        }

        .banner-slide-description {
            font-size: 0.9rem;
            margin-bottom: 10px;
        }

        .banner-slide-category {
            display: inline-block;
            padding: 3px 10px;
            background: var(--primary-color);
            border-radius: 15px;
            font-size: 0.8rem;
        }

        .banners-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .banner-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            flex-direction: column;
        }

        .banner-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .banner-image {
            height: 150px; /* کاهش ارتفاع تصاویر */
            width: 100%;
            object-fit: cover;
        }

        .banner-content {
            padding: 15px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .banner-title {
            font-size: 1.1rem;
            margin-bottom: 10px;
            color: var(--dark-text);
        }

        .banner-description {
            color: #666;
            margin-bottom: 15px;
            font-size: 0.9rem;
            flex-grow: 1;
        }

        .banner-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.85rem;
            color: #888;
        }

        .banner-category {
            display: inline-block;
            padding: 3px 8px;
            background: #f0f0f0;
            border-radius: 15px;
            font-size: 0.75rem;
        }

        /* دسته‌بندی‌ها */
        .categories-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 30px;
        }

        .category-card {
            background: white;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
            cursor: pointer;
        }

        .category-card:hover {
            transform: translateY(-5px);
        }

        .category-card i {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        .category-card h3 {
            margin-bottom: 10px;
            font-size: 1.2rem;
        }

        .category-card p {
            color: #666;
            font-size: 0.9rem;
        }

        /* صفحه چت */
        .chat-container {
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            overflow: hidden;
        }

        .chat-header {
            padding: 15px;
            background: var(--gradient);
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .chat-messages {
            height: 400px;
            overflow-y: auto;
            padding: 15px;
            background: #f9f9f9;
        }

        .message {
            margin-bottom: 15px;
            max-width: 80%;
        }

        .message-self {
            margin-left: auto;
        }

        .message-content {
            padding: 10px 15px;
            border-radius: 18px;
            background: white;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        .message-self .message-content {
            background: var(--primary-color);
            color: white;
        }

        .message-info {
            display: flex;
            justify-content: space-between;
            font-size: 0.75rem;
            margin-top: 5px;
            color: #888;
        }

        .message-self .message-info {
            color: rgba(255,255,255,0.8);
        }

        .chat-input {
            display: flex;
            padding: 15px;
            border-top: 1px solid #eee;
        }

        .chat-input input {
            flex: 1;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 20px;
            margin-left: 10px;
        }

        .chat-input button {
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            cursor: pointer;
        }

        /* صفحه پروفایل */
        .profile-card {
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            padding: 20px;
            margin-bottom: 20px;
        }

        .profile-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }

        .profile-avatar {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--primary-color);
            margin-left: 20px;
        }

        .profile-info h2 {
            margin-bottom: 5px;
        }

        .profile-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }

        .stat-item {
            text-align: center;
            padding: 15px;
            background: #f9f9f9;
            border-radius: 8px;
        }

        .stat-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-color);
        }

        .stat-label {
            font-size: 0.85rem;
            color: #888;
        }

        /* صفحه ادمین */
        .admin-panel {
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            padding: 20px;
            margin-bottom: 20px;
        }

        .admin-tabs {
            display: flex;
            border-bottom: 1px solid #eee;
            margin-bottom: 20px;
            overflow-x: auto;
        }

        .admin-tab {
            padding: 10px 15px;
            cursor: pointer;
            border-bottom: 3px solid transparent;
            white-space: nowrap;
        }

        .admin-tab.active {
            border-bottom: 3px solid var(--primary-color);
            color: var(--primary-color);
            font-weight: bold;
        }

        .admin-content {
            display: none;
        }

        .admin-content.active {
            display: block;
        }

        /* فرم افزودن/ویرایش بنر */
        .banner-form {
            background: #f9f9f9;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .admin-item {
            background: white;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 15px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        .admin-item-header {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }

        .admin-item-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            margin-left: 15px;
        }

        .admin-item-actions {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .btn-sm {
            padding: 5px 10px;
            font-size: 0.85rem;
        }

        /* دکمه پشتیبانی */
        .support-button {
            position: fixed;
            bottom: 20px;
            left: 20px;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 50px;
            padding: 12px 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            z-index: 1000;
            cursor: pointer;
            transition: all 0.3s;
        }

        .support-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.25);
        }

        .support-button i {
            margin-right: 8px;
        }

        /* صفحه‌بندی */
        .pagination {
            display: flex;
            justify-content: center;
            margin-top: 30px;
        }

        .page-item {
            margin: 0 5px;
        }

        .page-link {
            display: block;
            padding: 8px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            color: var(--dark-text);
            text-decoration: none;
            transition: all 0.3s;
        }

        .page-link:hover {
            background: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
        }

        .page-item.active .page-link {
            background: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
        }

        /* رسپانسیو */
        @media (max-width: 992px) {
            .categories-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .navbar-content {
                flex-direction: column;
            }
            
            .nav-links {
                margin-top: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .nav-links li {
                margin: 5px;
            }
            
            .banners-grid {
                grid-template-columns: 1fr;
            }
            
            .categories-grid {
                grid-template-columns: 1fr;
            }
            
            .profile-stats {
                grid-template-columns: 1fr;
            }
            
            .profile-header {
                flex-direction: column;
                text-align: center;
            }
            
            .profile-avatar {
                margin-left: 0;
                margin-bottom: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- صفحه ورود و ثبت نام -->
    <div class="auth-container" id="auth-page">
        <div class="auth-card">
            <div class="auth-header">
                <h1>لینکدونی</h1>
                <p>Link VIPZEXNET - یک دنیای متفاوت از لینک‌ها</p>
            </div>
            <div class="auth-body">
                <div class="auth-tabs">
                    <div class="auth-tab active" data-tab="login">ورود</div>
                    <div class="auth-tab" data-tab="register">ثبت نام</div>
                </div>
                
                <form id="login-form" class="auth-form active">
                    <div class="form-group">
                        <label class="form-label">نام کاربری</label>
                        <input type="text" class="form-control" id="login-username" required>
                        <div class="error-message" id="login-username-error">لطفا نام کاربری خود را وارد کنید</div>
                    </div>
                    <div class="form-group">
                        <label class="form-label">رمز عبور</label>
                        <input type="password" class="form-control" id="login-password" required>
                        <div class="error-message" id="login-password-error">لطفا رمز عبور خود را وارد کنید</div>
                    </div>
                    <div class="form-group">
                        <button type="submit" class="btn btn-primary">ورود به حساب</button>
                    </div>
                </form>
                
                <form id="register-form" class="auth-form">
                    <div class="form-group">
                        <label class="form-label">نام کاربری</label>
                        <input type="text" class="form-control" id="register-username" required>
                        <div class="error-message" id="register-username-error">لطفا یک نام کاربری انتخاب کنید</div>
                    </div>
                    <div class="form-group">
                        <label class="form-label">ایمیل</label>
                        <input type="email" class="form-control" id="register-email" required>
                        <div class="error-message" id="register-email-error">لطفا یک ایمیل معتبر وارد کنید</div>
                    </div>
                    <div class="form-group">
                        <label class="form-label">رمز عبور</label>
                        <input type="password" class="form-control" id="register-password" required>
                        <div class="error-message" id="register-password-error">لطفا یک رمز عبور انتخاب کنید</div>
                    </div>
                    <div class="form-group">
                        <label class="form-label">تکرار رمز عبور</label>
                        <input type="password" class="form-control" id="register-confirm-password" required>
                        <div class="error-message" id="register-confirm-password-error">رمز عبور و تکرار آن مطابقت ندارند</div>
                    </div>
                    <div class="form-group">
                        <button type="submit" class="btn btn-primary">ایجاد حساب کاربری</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- برنامه اصلی -->
    <div class="main-app" id="main-app">
        <!-- نوار ناوبری -->
        <nav class="navbar">
            <div class="container">
                <div class="navbar-content">
                    <div class="logo">
                        <i class="bi bi-link-45deg"></i>
                        <span>لینکدونی</span>
                    </div>
                    <ul class="nav-links">
                        <li><a href="#" data-page="home">صفحه اصلی</a></li>
                        <li><a href="#" data-page="banners">بنرها</a></li>
                        <li><a href="#" data-page="chat">چت</a></li>
                        <li><a href="#" data-page="profile">پروفایل</a></li>
                        <li><a href="#" id="admin-link" data-page="admin" style="display: none;">مدیریت</a></li>
                        <li><a href="#" id="logout-btn">خروج</a></li>
                    </ul>
                </div>
            </div>
        </nav>

        <!-- محتوای اصلی -->
        <div class="container main-content">
            <!-- صفحه اصلی -->
            <div class="page-content" id="home-page">
                <!-- اسلایدر بنرهای کشویی -->
                <div class="banners-slider" id="banners-slider">
                    <!-- بنرهای کشویی اینجا نمایش داده می شوند -->
                </div>
                
                <h2 class="section-title">دسته‌بندی‌ها</h2>
                <div class="categories-grid">
                    <div class="category-card" data-category="ربات">
                        <i class="bi bi-robot"></i>
                        <h3>ربات‌ها</h3>
                        <p>ربات‌های کاربردی و سرگرم کننده</p>
                    </div>
                    <div class="category-card" data-category="گروه">
                        <i class="bi bi-people-fill"></i>
                        <h3>گروه‌ها</h3>
                        <p>گروه‌های فعال و پربار</p>
                    </div>
                    <div class="category-card" data-category="کانال">
                        <i class="bi bi-megaphone"></i>
                        <h3>کانال‌ها</h3>
                        <p>کانال‌های اطلاع‌رسانی و خبری</p>
                    </div>
                </div>
                
                <h2 class="section-title">بنرهای پرطرفدار</h2>
                <div class="banners-grid" id="featured-banners">
                    <!-- بنرهای پرطرفدار اینجا نمایش داده می شوند -->
                </div>
            </div>

            <!-- صفحه بنرها -->
            <div class="page-content" id="banners-page" style="display: none;">
                <h2 class="section-title">همه بنرها</h2>
                <div class="banners-grid" id="all-banners">
                    <!-- همه بنرها اینجا نمایش داده می شوند -->
                </div>
                
                <!-- صفحه‌بندی -->
                <nav class="pagination-container">
                    <ul class="pagination" id="banners-pagination">
                        <!-- صفحه‌بندی اینجا نمایش داده می شود -->
                    </ul>
                </nav>
            </div>

            <!-- صفحه چت -->
            <div class="page-content" id="chat-page" style="display: none;">
                <div class="chat-container">
                    <div class="chat-header">
                        <h3>چت روم</h3>
                        <span>آنلاین: <span id="online-users">۱۲</span> کاربر</span>
                    </div>
                    <div class="chat-messages" id="chat-messages">
                        <!-- پیام‌های چت اینجا نمایش داده می شوند -->
                    </div>
                    <div class="chat-input">
                        <input type="text" id="chat-input" placeholder="پیام خود را بنویسید...">
                        <button id="send-message"><i class="bi bi-send"></i></button>
                    </div>
                </div>
            </div>

            <!-- صفحه پروفایل -->
            <div class="page-content" id="profile-page" style="display: none;">
                <div class="profile-card">
                    <div class="profile-header">
                        <img src="https://ui-avatars.com/api/?name=کاربر+لینکدونی&size=100&background=3498db&color=fff" class="profile-avatar" id="profile-avatar">
                        <div class="profile-info">
                            <h2 id="profile-name">کاربر لینکدونی</h2>
                            <p id="profile-username">@user123</p>
                        </div>
                    </div>
                    
                    <div class="profile-stats">
                        <div class="stat-item">
                            <div class="stat-value" id="profile-banners">۰</div>
                            <div class="stat-label">بنرها</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="profile-messages">۰</div>
                            <div class="stat-label">پیام‌ها</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="profile-likes">۰</div>
                            <div class="stat-label">لایک‌ها</div>
                        </div>
                    </div>
                    
                    <div class="profile-details">
                        <h3>اطلاعات حساب</h3>
                        <div class="detail-item">
                            <span>ایمیل:</span>
                            <span id="profile-email">user@linkoni.ir</span>
                        </div>
                        <div class="detail-item">
                            <span>تاریخ عضویت:</span>
                            <span id="profile-join-date">۱۴۰۲/۰۵/۰۱</span>
                        </div>
                        <div class="detail-item">
                            <span>وضعیت حساب:</span>
                            <span id="profile-status" class="badge bg-success">فعال</span>
                        </div>
                    </div>
                </div>
                
                <!-- بنرهای کاربر -->
                <h3 class="section-title">بنرهای من</h3>
                <div class="banners-grid" id="user-banners">
                    <!-- بنرهای کاربر اینجا نمایش داده می شوند -->
                </div>
            </div>

            <!-- صفحه مدیریت -->
            <div class="page-content" id="admin-page" style="display: none;">
                <div class="admin-panel">
                    <div class="admin-tabs">
                        <div class="admin-tab active" data-tab="users">مدیریت کاربران</div>
                        <div class="admin-tab" data-tab="banners">مدیریت بنرها</div>
                        <div class="admin-tab" data-tab="add-banner">افزودن بنر</div>
                        <div class="admin-tab" data-tab="reports">گزارش‌ها</div>
                    </div>
                    
                    <div class="admin-content active" id="admin-users">
                        <h3>مدیریت کاربران</h3>
                        <div class="users-list" id="admin-users-list">
                            <!-- لیست کاربران برای مدیریت -->
                        </div>
                    </div>
                    
                    <div class="admin-content" id="admin-banners">
                        <h3>مدیریت بنرها</h3>
                        <div class="banners-list" id="admin-banners-list">
                            <!-- لیست بنرها برای مدیریت -->
                        </div>
                    </div>
                    
                    <div class="admin-content" id="admin-add-banner">
                        <h3>افزودن بنر جدید</h3>
                        <form id="add-banner-form" class="banner-form">
                            <div class="form-group">
                                <label class="form-label">عنوان بنر</label>
                                <input type="text" class="form-control" id="banner-title" required>
                            </div>
                            <div class="form-group">
                                <label class="form-label">توضیحات</label>
                                <textarea class="form-control" id="banner-description" rows="3" required></textarea>
                            </div>
                            <div class="form-group">
                                <label class="form-label">آدرس تصویر</label>
                                <input type="url" class="form-control" id="banner-image" required>
                            </div>
                            <div class="form-group">
                                <label class="form-label">لینک</label>
                                <input type="url" class="form-control" id="banner-url" required>
                            </div>
                            <div class="form-group">
                                <label class="form-label">دسته‌بندی</label>
                                <select class="form-control" id="banner-category" required>
                                    <option value="">انتخاب دسته‌بندی</option>
                                    <option value="ربات">ربات</option>
                                    <option value="گروه">گروه</option>
                                    <option value="کانال">کانال</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <button type="submit" class="btn btn-primary">افزودن بنر</button>
                            </div>
                        </form>
                    </div>
                    
                    <div class="admin-content" id="admin-reports">
                        <h3>گزارش‌ها</h3>
                        <div class="reports-list" id="admin-reports-list">
                            <!-- لیست گزارش‌ها -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- دکمه پشتیبانی -->
    <button class="support-button" onclick="openSupport()">
        <i class="bi bi-headset"></i> پشتیبانی
    </button>

    <!-- مودال ویرایش بنر -->
    <div class="modal fade" id="editBannerModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title">ویرایش بنر</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="edit-banner-form">
                        <input type="hidden" id="edit-banner-id">
                        <div class="form-group">
                            <label class="form-label">عنوان بنر</label>
                            <input type="text" class="form-control" id="edit-banner-title" required>
                        </div>
                        <div class="form-group">
                            <label class="form-label">توضیحات</label>
                            <textarea class="form-control" id="edit-banner-description" rows="3" required></textarea>
                        </div>
                        <div class="form-group">
                            <label class="form-label">آدرس تصویر</label>
                            <input type="url" class="form-control" id="edit-banner-image" required>
                        </div>
                        <div class="form-group">
                            <label class="form-label">لینک</label>
                            <input type="url" class="form-control" id="edit-banner-url" required>
                        </div>
                        <div class="form-group">
                            <label class="form-label">دسته‌بندی</label>
                            <select class="form-control" id="edit-banner-category" required>
                                <option value="ربات">ربات</option>
                                <option value="گروه">گروه</option>
                                <option value="کانال">کانال</option>
                            </select>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">لغو</button>
                    <button type="button" class="btn btn-primary" id="save-banner-changes">ذخیره تغییرات</button>
                </div>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // داده‌های نمونه
        let users = [
            { 
                id: 1,
                username: "user123", 
                password: "pass123", 
                email: "user@linkoni.ir",
                name: "کاربر نمونه",
                avatar: "https://ui-avatars.com/api/?name=کاربر+نمونه&size=100&background=3498db&color=fff",
                joinDate: "1402/05/01",
                bannersCount: 2,
                messagesCount: 15,
                likesCount: 42,
                isAdmin: false,
                isBlocked: false
            },
            { 
                id: 2,
                username: "admin", 
                password: "admin123", 
                email: "admin@linkoni.ir",
                name: "مدیر سیستم",
                avatar: "https://ui-avatars.com/api/?name=مدیر+سیستم&size=100&background=e74c3c&color=fff",
                joinDate: "1402/01/01",
                bannersCount: 5,
                messagesCount: 89,
                likesCount: 126,
                isAdmin: true,
                isBlocked: false
            }
        ];

        let banners = [
            {
                id: 1,
                title: "ربات چت ناشناس",
                description: "چتوگرام - ربات چت ناشناس برای ارتباطات امن و خصوصی",
                image: "https://via.placeholder.com/600x300/3498db/ffffff?text=ربات+چت+ناشناس",
                url: "#",
                category: "ربات",
                likes: 32,
                userId: 1
            },
            {
                id: 2,
                title: "گروه برنامه نویسی",
                description: "گروه تخصصی برنامه نویسی و تبادل اطلاعات",
                image: "https://via.placeholder.com/600x300/2ecc71/ffffff?text=گروه+برنامه+نویسی",
                url: "#",
                category: "گروه",
                likes: 24,
                userId: 2
            },
            {
                id: 3,
                title: "کانال خبری فناوری",
                description: "اخبار روز فناوری و تکنولوژی",
                image: "https://via.placeholder.com/600x300/e74c3c/ffffff?text=کانال+خبری+فناوری",
                url: "#",
                category: "کانال",
                likes: 18,
                userId: 1
            }
        ];

        let currentUser = null;
        let currentBannerPage = 1;
        const bannersPerPage = 6;

        // ذخیره داده‌ها در localStorage
        function saveData() {
            localStorage.setItem('users', JSON.stringify(users));
            localStorage.setItem('banners', JSON.stringify(banners));
            if (currentUser) {
                localStorage.setItem('currentUser', JSON.stringify(currentUser));
            }
        }

        // بارگذاری داده‌ها از localStorage
        function loadData() {
            const savedUsers = localStorage.getItem('users');
            const savedBanners = localStorage.getItem('banners');
            const savedCurrentUser = localStorage.getItem('currentUser');
            
            if (savedUsers) users = JSON.parse(savedUsers);
            if (savedBanners) banners = JSON.parse(savedBanners);
            if (savedCurrentUser) currentUser = JSON.parse(savedCurrentUser);
        }

        // نمایش صفحه مورد نظر
        function showPage(pageId) {
            // مخفی کردن همه صفحات
            document.querySelectorAll('.page-content').forEach(page => {
                page.style.display = 'none';
            });
            
            // نمایش صفحه درخواستی
            document.getElementById(pageId + '-page').style.display = 'block';
            
            // بارگذاری محتوای صفحه
            if (pageId === 'home') {
                loadBannerSlider();
                loadFeaturedBanners();
            } else if (pageId === 'banners') {
                loadAllBanners();
                setupBannersPagination();
            } else if (pageId === 'chat') {
                loadChatMessages();
            } else if (pageId === 'profile') {
                loadProfile();
                loadUserBanners();
            } else if (pageId === 'admin') {
                loadAdminPanel();
            }
        }

        // بارگذاری اسلایدر بنرها
        function loadBannerSlider() {
            const container = document.getElementById('banners-slider');
            container.innerHTML = '';
            
            // مرتب کردن بنرها بر اساس تعداد لایک
            const featuredBanners = [...banners].sort((a, b) => b.likes - a.likes).slice(0, 5);
            
            featuredBanners.forEach((banner, index) => {
                const bannerElement = `
                    <div class="banner-slide ${index === 0 ? 'active' : ''}" style="background-image: url('${banner.image}')">
                        <div class="banner-info">
                            <h3 class="banner-slide-title">${banner.title}</h3>
                            <p class="banner-slide-description">${banner.description}</p>
                            <span class="banner-slide-category">${banner.category}</span>
                        </div>
                    </div>
                `;
                container.innerHTML += bannerElement;
            });
            
            // راه اندازی خودکار اسلایدر
            startBannerSlider();
        }

        // راه اندازی اسلایدر بنرها
        function startBannerSlider() {
            const slides = document.querySelectorAll('.banner-slide');
            let currentSlide = 0;
            
            setInterval(() => {
                slides[currentSlide].classList.remove('active');
                currentSlide = (currentSlide + 1) % slides.length;
                slides[currentSlide].classList.add('active');
            }, 5000);
        }

        // بارگذاری بنرهای پرطرفدار
        function loadFeaturedBanners() {
            const container = document.getElementById('featured-banners');
            container.innerHTML = '';
            
            // مرتب کردن بنرها بر اساس تعداد لایک
            const featuredBanners = [...banners].sort((a, b) => b.likes - a.likes).slice(0, 3);
            
            featuredBanners.forEach(banner => {
                const bannerElement = `
                    <div class="banner-card">
                        <img src="${banner.image}" class="banner-image" alt="${banner.title}">
                        <div class="banner-content">
                            <h3 class="banner-title">${banner.title}</h3>
                            <p class="banner-description">${banner.description}</p>
                            <div class="banner-meta">
                                <span class="banner-category">${banner.category}</span>
                                <span><i class="bi bi-heart-fill"></i> ${banner.likes}</span>
                            </div>
                        </div>
                    </div>
                `;
                container.innerHTML += bannerElement;
            });
        }

        // بارگذاری همه بنرها با صفحه‌بندی
        function loadAllBanners(page = 1) {
            const container = document.getElementById('all-banners');
            container.innerHTML = '';
            
            currentBannerPage = page;
            const startIndex = (page - 1) * bannersPerPage;
            const endIndex = startIndex + bannersPerPage;
            const bannersToShow = banners.slice(startIndex, endIndex);
            
            bannersToShow.forEach(banner => {
                const bannerElement = `
                    <div class="banner-card">
                        <img src="${banner.image}" class="banner-image" alt="${banner.title}">
                        <div class="banner-content">
                            <h3 class="banner-title">${banner.title}</h3>
                            <p class="banner-description">${banner.description}</p>
                            <div class="banner-meta">
                                <span class="banner-category">${banner.category}</span>
                                <span><i class="bi bi-heart-fill"></i> ${banner.likes}</span>
                            </div>
                        </div>
                    </div>
                `;
                container.innerHTML += bannerElement;
            });
        }

        // تنظیم صفحه‌بندی بنرها
        function setupBannersPagination() {
            const totalPages = Math.ceil(banners.length / bannersPerPage);
            const paginationContainer = document.getElementById('banners-pagination');
            paginationContainer.innerHTML = '';
            
            if (totalPages <= 1) return;
            
            // دکمه قبلی
            if (currentBannerPage > 1) {
                paginationContainer.innerHTML += `
                    <li class="page-item">
                        <a class="page-link" href="#" onclick="loadAllBanners(${currentBannerPage - 1}); return false;">قبلی</a>
                    </li>
                `;
            }
            
            // صفحات
            for (let i = 1; i <= totalPages; i++) {
                paginationContainer.innerHTML += `
                    <li class="page-item ${i === currentBannerPage ? 'active' : ''}">
                        <a class="page-link" href="#" onclick="loadAllBanners(${i}); return false;">${i}</a>
                    </li>
                `;
            }
            
            // دکمه بعدی
            if (currentBannerPage < totalPages) {
                paginationContainer.innerHTML += `
                    <li class="page-item">
                        <a class="page-link" href="#" onclick="loadAllBanners(${currentBannerPage + 1}); return false;">بعدی</a>
                    </li>
                `;
            }
        }

        // بارگذاری پیام‌های چت
        function loadChatMessages() {
            const container = document.getElementById('chat-messages');
            container.innerHTML = '';
            
            // پیام‌های نمونه
            const sampleMessages = [
                { user: "مدیر سیستم", message: "به چت روم لینکدونی خوش آمدید!", time: "۱۰:۳۰", self: false },
                { user: "کاربر مهمان", message: "سلام. چت روم خیلی خوبی دارید.", time: "۱۰:۳۲", self: false },
                { user: "شما", message: "سلام. ممنون از توجه شما.", time: "۱۰:۳۳", self: true }
            ];
            
            sampleMessages.forEach(msg => {
                const messageElement = `
                    <div class="message ${msg.self ? 'message-self' : ''}">
                        <div class="message-content">${msg.message}</div>
                        <div class="message-info">
                            <span>${msg.user}</span>
                            <span>${msg.time}</span>
                        </div>
                    </div>
                `;
                container.innerHTML += messageElement;
            });
            
            // اسکرول به پایین
            container.scrollTop = container.scrollHeight;
        }

        // بارگذاری پروفایل کاربر
        function loadProfile() {
            if (currentUser) {
                document.getElementById('profile-name').textContent = currentUser.name;
                document.getElementById('profile-username').textContent = '@' + currentUser.username;
                document.getElementById('profile-email').textContent = currentUser.email;
                document.getElementById('profile-join-date').textContent = currentUser.joinDate;
                document.getElementById('profile-banners').textContent = currentUser.bannersCount;
                document.getElementById('profile-messages').textContent = currentUser.messagesCount;
                document.getElementById('profile-likes').textContent = currentUser.likesCount;
                document.getElementById('profile-avatar').src = currentUser.avatar;
                
                if (currentUser.isAdmin) {
                    document.getElementById('admin-link').style.display = 'block';
                }
            }
        }

        // بارگذاری بنرهای کاربر
        function loadUserBanners() {
            if (!currentUser) return;
            
            const container = document.getElementById('user-banners');
            container.innerHTML = '';
            
            const userBanners = banners.filter(banner => banner.userId === currentUser.id);
            
            if (userBanners.length === 0) {
                container.innerHTML = '<p class="text-center">شما هنوز بنری اضافه نکرده‌اید.</p>';
                return;
            }
            
            userBanners.forEach(banner => {
                const bannerElement = `
                    <div class="banner-card">
                        <img src="${banner.image}" class="banner-image" alt="${banner.title}">
                        <div class="banner-content">
                            <h3 class="banner-title">${banner.title}</h3>
                            <p class="banner-description">${banner.description}</p>
                            <div class="banner-meta">
                                <span class="banner-category">${banner.category}</span>
                                <span><i class="bi bi-heart-fill"></i> ${banner.likes}</span>
                            </div>
                        </div>
                    </div>
                `;
                container.innerHTML += bannerElement;
            });
        }

        // بارگذاری پنل مدیریت
        function loadAdminPanel() {
            // فقط برای ادمین‌ها قابل دسترسی است
            if (!currentUser || !currentUser.isAdmin) {
                showPage('home');
                return;
            }
            
            // بارگذاری لیست کاربران
            const usersList = document.getElementById('admin-users-list');
            usersList.innerHTML = '';
            
            users.forEach(user => {
                const userElement = `
                    <div class="admin-item">
                        <div class="admin-item-header">
                            <img src="${user.avatar}" class="admin-item-avatar">
                            <div class="admin-item-info">
                                <h4>${user.name}</h4>
                                <p>@${user.username}</p>
                            </div>
                        </div>
                        <div class="admin-item-stats">
                            <span>بنرها: ${user.bannersCount}</span>
                            <span>پیام‌ها: ${user.messagesCount}</span>
                        </div>
                        <div class="admin-item-actions">
                            ${!user.isAdmin ? `<button class="btn btn-sm btn-primary" onclick="makeAdmin(${user.id})">تبدیل به ادمین</button>` : ''}
                            ${user.isBlocked ? 
                                `<button class="btn btn-sm btn-success" onclick="toggleBlockUser(${user.id})">رفع مسدودیت</button>` : 
                                `<button class="btn btn-sm btn-warning" onclick="toggleBlockUser(${user.id})">مسدود کردن</button>`
                            }
                        </div>
                    </div>
                `;
                usersList.innerHTML += userElement;
            });
            
            // بارگذاری لیست بنرها برای مدیریت
            const bannersList = document.getElementById('admin-banners-list');
            bannersList.innerHTML = '';
            
            banners.forEach(banner => {
                const user = users.find(u => u.id === banner.userId);
                const bannerElement = `
                    <div class="admin-item">
                        <div class="admin-item-header">
                            <img src="${banner.image}" class="admin-item-avatar" style="object-fit: cover; height: 60px; width: 60px;">
                            <div class="admin-item-info">
                                <h4>${banner.title}</h4>
                                <p>دسته‌بندی: ${banner.category} | لایک: ${banner.likes}</p>
                                <p>توسط: ${user ? user.name : 'ناشناس'}</p>
                            </div>
                        </div>
                        <div class="admin-item-actions">
                            <button class="btn btn-sm btn-primary" onclick="editBanner(${banner.id})">ویرایش</button>
                            <button class="btn btn-sm btn-danger" onclick="deleteBanner(${banner.id})">حذف</button>
                        </div>
                    </div>
                `;
                bannersList.innerHTML += bannerElement;
            });
        }

        // تبدیل کاربر به ادمین
        function makeAdmin(userId) {
            const user = users.find(u => u.id === userId);
            if (user) {
                user.isAdmin = true;
                saveData();
                loadAdminPanel();
                showNotification(`کاربر ${user.name} به ادمین تبدیل شد.`, 'success');
            }
        }

        // مسدود کردن یا رفع مسدودیت کاربر
        function toggleBlockUser(userId) {
            const user = users.find(u => u.id === userId);
            if (user) {
                user.isBlocked = !user.isBlocked;
                saveData();
                loadAdminPanel();
                
                if (user.isBlocked) {
                    showNotification(`کاربر ${user.name} مسدود شد.`, 'success');
                } else {
                    showNotification(`مسدودیت کاربر ${user.name} برداشته شد.`, 'success');
                }
            }
        }

        // افزودن بنر جدید
        function addBanner(title, description, image, url, category) {
            const newBanner = {
                id: banners.length > 0 ? Math.max(...banners.map(b => b.id)) + 1 : 1,
                title: title,
                description: description,
                image: image,
                url: url,
                category: category,
                likes: 0,
                userId: currentUser.id
            };
            
            banners.push(newBanner);
            
            // افزایش شمارنده بنرهای کاربر
            if (currentUser) {
                currentUser.bannersCount++;
                saveData();
                document.getElementById('profile-banners').textContent = currentUser.bannersCount;
            }
            
            saveData();
            showNotification('بنر جدید با موفقیت اضافه شد.', 'success');
            
            // بازگشت به صفحه مدیریت بنرها
            document.querySelector('.admin-tab[data-tab="banners"]').click();
            loadAdminPanel();
        }

        // ویرایش بنر
        function editBanner(bannerId) {
            const banner = banners.find(b => b.id === bannerId);
            if (!banner) return;
            
            // پر کردن فرم ویرایش
            document.getElementById('edit-banner-id').value = banner.id;
            document.getElementById('edit-banner-title').value = banner.title;
            document.getElementById('edit-banner-description').value = banner.description;
            document.getElementById('edit-banner-image').value = banner.image;
            document.getElementById('edit-banner-url').value = banner.url;
            document.getElementById('edit-banner-category').value = banner.category;
            
            // نمایش مودال
            const modal = new bootstrap.Modal(document.getElementById('editBannerModal'));
            modal.show();
        }

        // ذخیره تغییرات بنر
        function saveBannerChanges() {
            const bannerId = parseInt(document.getElementById('edit-banner-id').value);
            const banner = banners.find(b => b.id === bannerId);
            
            if (banner) {
                banner.title = document.getElementById('edit-banner-title').value;
                banner.description = document.getElementById('edit-banner-description').value;
                banner.image = document.getElementById('edit-banner-image').value;
                banner.url = document.getElementById('edit-banner-url').value;
                banner.category = document.getElementById('edit-banner-category').value;
                
                saveData();
                
                // بستن مودال
                const modal = bootstrap.Modal.getInstance(document.getElementById('editBannerModal'));
                modal.hide();
                
                showNotification('تغییرات بنر با موفقیت ذخیره شد.', 'success');
                loadAdminPanel();
            }
        }

        // حذف بنر
        function deleteBanner(bannerId) {
            if (confirm('آیا از حذف این بنر اطمینان دارید؟')) {
                const bannerIndex = banners.findIndex(b => b.id === bannerId);
                if (bannerIndex !== -1) {
                    banners.splice(bannerIndex, 1);
                    saveData();
                    showNotification('بنر با موفقیت حذف شد.', 'success');
                    loadAdminPanel();
                }
            }
        }

        // اعتبارسنجی فرم
        function validateForm(formId) {
            const form = document.getElementById(formId);
            const inputs = form.querySelectorAll('input[required]');
            let isValid = true;
            
            inputs.forEach(input => {
                const errorElement = document.getElementById(input.id + '-error');
                if (!input.value.trim()) {
                    if (errorElement) {
                        errorElement.style.display = 'block';
                    }
                    isValid = false;
                } else {
                    if (errorElement) {
                        errorElement.style.display = 'none';
                    }
                }
                
                // اعتبارسنجی خاص برای ایمیل
                if (input.type === 'email' && input.value.trim()) {
                    const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                    if (!emailPattern.test(input.value)) {
                        document.getElementById(input.id + '-error').style.display = 'block';
                        document.getElementById(input.id + '-error').textContent = 'لطفا یک ایمیل معتبر وارد کنید';
                        isValid = false;
                    }
                }
            });
            
            // اعتبارسنجی تطابق رمز عبور برای فرم ثبت نام
            if (formId === 'register-form') {
                const password = document.getElementById('register-password').value;
                const confirmPassword = document.getElementById('register-confirm-password').value;
                
                if (password !== confirmPassword) {
                    document.getElementById('register-confirm-password-error').style.display = 'block';
                    isValid = false;
                }
            }
            
            return isValid;
        }

        // نمایش نوتیفیکیشن
        function showNotification(message, type) {
            // ایجاد المان نوتیفیکیشن
            const notification = document.createElement('div');
            notification.className = `notification notification-${type}`;
            notification.style.cssText = `
                position: fixed;
                top: 20px;
                right: 20px;
                background: ${type === 'success' ? '#2ecc71' : '#e74c3c'};
                color: white;
                padding: 15px 20px;
                border-radius: 5px;
                box-shadow: 0 4px 15px rgba(0,0,0,0.2);
                z-index: 1050;
                display: flex;
                align-items: center;
            `;
            
            notification.innerHTML = `
                <div class="notification-content">
                    <i class="bi ${type === 'success' ? 'bi-check-circle' : 'bi-exclamation-circle'}" style="margin-left: 10px;"></i>
                    <span>${message}</span>
                </div>
            `;
            
            document.body.appendChild(notification);
            
            // حذف خودکار پس از 3 ثانیه
            setTimeout(() => {
                if (notification.parentNode) {
                    notification.parentNode.removeChild(notification);
                }
            }, 3000);
        }

        // باز کردن پشتیبانی
        function openSupport() {
            alert('سیستم پشتیبانی در حال حاضر در دسترس نیست. لطفا稍后再试。');
        }

        // مدیریت رویدادهای صفحه
        document.addEventListener('DOMContentLoaded', function() {
            // بارگذاری داده‌ها
            loadData();
            
            // اگر کاربر قبلا وارد شده بود، برنامه اصلی را نشان بده
            if (currentUser) {
                document.getElementById('auth-page').style.display = 'none';
                document.getElementById('main-app').style.display = 'block';
                loadProfile();
                showPage('home');
            }
            
            // مدیریت تب‌های فرم ورود/ثبت نام
            document.querySelectorAll('.auth-tab').forEach(tab => {
                tab.addEventListener('click', function() {
                    const tabId = this.getAttribute('data-tab');
                    
                    // غیرفعال کردن همه تب‌ها
                    document.querySelectorAll('.auth-tab').forEach(t => {
                        t.classList.remove('active');
                    });
                    
                    // فعال کردن تب انتخاب شده
                    this.classList.add('active');
                    
                    // مخفی کردن همه فرم‌ها
                    document.querySelectorAll('.auth-form').forEach(form => {
                        form.classList.remove('active');
                    });
                    
                    // نمایش فرم مربوطه
                    document.getElementById(tabId + '-form').classList.add('active');
                });
            });
            
            // مدیریت فرم ورود
            document.getElementById('login-form').addEventListener('submit', function(e) {
                e.preventDefault();
                
                if (!validateForm('login-form')) {
                    return;
                }
                
                const username = document.getElementById('login-username').value;
                const password = document.getElementById('login-password').value;
                
                const user = users.find(u => u.username === username && u.password === password);
                
                if (user) {
                    if (user.isBlocked) {
                        showNotification('حساب کاربری شما مسدود شده است.', 'error');
                        return;
                    }
                    
                    currentUser = user;
                    saveData();
                    
                    document.getElementById('auth-page').style.display = 'none';
                    document.getElementById('main-app').style.display = 'block';
                    
                    showNotification(`خوش آمدید ${user.name}`, 'success');
                    loadProfile();
                    showPage('home');
                } else {
                    showNotification('نام کاربری یا رمز عبور اشتباه است.', 'error');
                }
            });
            
            // مدیریت فرم ثبت نام
            document.getElementById('register-form').addEventListener('submit', function(e) {
                e.preventDefault();
                
                if (!validateForm('register-form')) {
                    return;
                }
                
                const username = document.getElementById('register-username').value;
                const email = document.getElementById('register-email').value;
                const password = document.getElementById('register-password').value;
                
                if (users.find(u => u.username === username)) {
                    showNotification('این نام کاربری قبلا ثبت شده است.', 'error');
                    return;
                }
                
                const newUser = {
                    id: users.length > 0 ? Math.max(...users.map(u => u.id)) + 1 : 1,
                    username: username,
                    password: password,
                    email: email,
                    name: username,
                    avatar: `https://ui-avatars.com/api/?name=${encodeURIComponent(username)}&size=100&background=3498db&color=fff`,
                    joinDate: new Date().toLocaleDateString('fa-IR'),
                    bannersCount: 0,
                    messagesCount: 0,
                    likesCount: 0,
                    isAdmin: false,
                    isBlocked: false
                };
                
                users.push(newUser);
                currentUser = newUser;
                saveData();
                
                document.getElementById('auth-page').style.display = 'none';
                document.getElementById('main-app').style.display = 'block';
                
                showNotification('ثبت نام با موفقیت انجام شد.', 'success');
                loadProfile();
                showPage('home');
            });
            
            // مدیریت منوی ناوبری
            document.querySelectorAll('.nav-links a[data-page]').forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const pageId = this.getAttribute('data-page');
                    showPage(pageId);
                });
            });
            
            // مدیریت دکمه خروج
            document.getElementById('logout-btn').addEventListener('click', function(e) {
                e.preventDefault();
                currentUser = null;
                localStorage.removeItem('currentUser');
                
                document.getElementById('main-app').style.display = 'none';
                document.getElementById('auth-page').style.display = 'flex';
                
                showNotification('با موفقیت خارج شدید.', 'success');
            });
            
            // مدیریت تب‌های مدیریت
            document.querySelectorAll('.admin-tab').forEach(tab => {
                tab.addEventListener('click', function() {
                    const tabId = this.getAttribute('data-tab');
                    
                    // غیرفعال کردن همه تب‌ها
                    document.querySelectorAll('.admin-tab').forEach(t => {
                        t.classList.remove('active');
                    });
                    
                    // فعال کردن تب انتخاب شده
                    this.classList.add('active');
                    
                    // مخفی کردن همه محتواها
                    document.querySelectorAll('.admin-content').forEach(content => {
                        content.classList.remove('active');
                    });
                    
                    // نمایش محتوای مربوطه
                    document.getElementById('admin-' + tabId).classList.add('active');
                });
            });
            
            // مدیریت ارسال پیام در چت
            document.getElementById('send-message').addEventListener('click', function() {
                const input = document.getElementById('chat-input');
                const message = input.value.trim();
                
                if (message) {
                    const now = new Date();
                    const time = `${now.getHours()}:${now.getMinutes().toString().padStart(2, '0')}`;
                    
                    const messageElement = `
                        <div class="message message-self">
                            <div class="message-content">${message}</div>
                            <div class="message-info">
                                <span>شما</span>
                                <span>${time}</span>
                            </div>
                        </div>
                    `;
                    
                    document.getElementById('chat-messages').innerHTML += messageElement;
                    input.value = '';
                    
                    // اسکرول به پایین
                    const container = document.getElementById('chat-messages');
                    container.scrollTop = container.scrollHeight;
                    
                    // افزایش شمارنده پیام‌های کاربر
                    if (currentUser) {
                        currentUser.messagesCount++;
                        saveData();
                        document.getElementById('profile-messages').textContent = currentUser.messagesCount;
                    }
                }
            });
            
            // امکان ارسال پیام با کلید Enter
            document.getElementById('chat-input').addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    document.getElementById('send-message').click();
                }
            });
            
            // مدیریت فرم افزودن بنر
            document.getElementById('add-banner-form').addEventListener('submit', function(e) {
                e.preventDefault();
                
                const title = document.getElementById('banner-title').value;
                const description = document.getElementById('banner-description').value;
                const image = document.getElementById('banner-image').value;
                const url = document.getElementById('banner-url').value;
                const category = document.getElementById('banner-category').value;
                
                addBanner(title, description, image, url, category);
                
                // پاک کردن فرم
                this.reset();
            });
            
            // مدیریت ذخیره تغییرات بنر
            document.getElementById('save-banner-changes').addEventListener('click', function() {
                saveBannerChanges();
            });
            
            // فیلتر کردن بنرها بر اساس دسته‌بندی
            document.querySelectorAll('.category-card').forEach(card => {
                card.addEventListener('click', function() {
                    const category = this.getAttribute('data-category');
                    showPage('banners');
                    
                    // فیلتر کردن بنرها بر اساس دسته‌بندی
                    const filteredBanners = banners.filter(banner => banner.category === category);
                    
                    const container = document.getElementById('all-banners');
                    container.innerHTML = '';
                    
                    if (filteredBanners.length === 0) {
                        container.innerHTML = `<p class="text-center">هیچ بنری در دسته‌بندی ${category} یافت نشد.</p>`;
                        document.getElementById('banners-pagination').innerHTML = '';
                        return;
                    }
                    
                    filteredBanners.forEach(banner => {
                        const bannerElement = `
                            <div class="banner-card">
                                <img src="${banner.image}" class="banner-image" alt="${banner.title}">
                                <div class="banner-content">
                                    <h3 class="banner-title">${banner.title}</h3>
                                    <p class="banner-description">${banner.description}</p>
                                    <div class="banner-meta">
                                        <span class="banner-category">${banner.category}</span>
                                        <span><i class="bi bi-heart-fill"></i> ${banner.likes}</span>
                                    </div>
                                </div>
                            </div>
                        `;
                        container.innerHTML += bannerElement;
                    });
                    
                    // مخفی کردن صفحه‌بندی
                    document.getElementById('banners-pagination').innerHTML = '';
                });
            });
        });
    </script>
</body>
</html>
