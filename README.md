
<!DOCTYPE html>
<html lang="fa" dir="rtl">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نرم افزار مدیریت مشتری آپدیت</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.rtl.min.css" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css">

    <!-- Vazirmatn Google Font -->
    <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@100..900&display=swap" rel="stylesheet">

    <style>

        *, *::before, *::after {
            box-sizing: border-box;
        }
        body {
            font-family: 'Vazirmatn', sans-serif;
            font-size: 12px;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        
        a {
            text-decoration: none;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #0078d4 0%, #106ebe 100%);
            color: white;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(0,0,0,0.15);
        }

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 6px 25px;
            background: rgba(0,0,0,0.1);
            font-size: 12px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .header-main {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 14px 25px;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 22px;
            font-weight: 700;
        }

        .logo i {
            font-size: 28px;
        }
        .ribbon {
            background: #f8f9fa;
            border-bottom: 1px solid #dee2e6;
            margin-top: 100px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }


        .card {
            box-shadow: 0 4px 24px rgba(0,78,146,0.07), 0 1.5px 6px rgba(0,0,0,0.04);
            border-radius: 14px;
            border: none;
        }
        .card-header {
            background-color: #e3ecf9;
            padding: 10px 16px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #b0c4de;
            border-radius: 14px 14px 0 0;
            font-weight: 600;
        }

        .footer {
            background: #e3ecf9;
            color: #334e6f;
            text-align: center;
            padding: 10px 0 6px 0;
            border-top: 1px solid #b0c4de;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.03);
            letter-spacing: 0.02em;
            position: fixed;
            right: 0;
            left: 0;
            bottom: 0;
            z-index: 1000;
        }
        body {
            padding-bottom: 80px;
        }
        .footer .social-icons {
            margin-top: 8px;
        }
        .footer .social-icons a {
            color: #004e92;
            margin: 0 7px;
            transition: color 0.2s;
        }
        .footer .social-icons a:hover {
            color: #000428;
        }
        @media (max-width: 768px) {
            .header, .sub-header, .card-header, .card-body, .toolbar {
                padding: 10px 8px !important;
            }
            .footer {
                padding: 12px 0 6px 0;
            }
        }
        .toolbar-btn.flex-column {
        flex-direction: column !important;
        align-items: center !important;
        justify-content: center;
        min-width: 72px;
        min-height: 62px;
        padding: 8px 8px 4px 8px;
        text-align: center;
    }
    .toolbar-btn.flex-column i {
        margin-bottom: 4px;
    }
    .toolbar-btn.flex-column span {
        display: block;
        margin-top: 0px;
    }
    .word-toolbar {
            direction: rtl;
            background: #f6f8fb;
            border-bottom: 1.5px solid #d3e2f7;
        }
        .toolbar-btn {
            background: #fff;
            border: 1.5px solid #e9eaf2;
            color: #2b579a;
            border-radius: 8px;
            font-family: inherit;
            padding: 7px 18px 7px 14px;
            margin-left: 2px;
            margin-right: 2px;
            transition: box-shadow 0.18s, border-color 0.18s, background 0.18s, color 0.18s;
            box-shadow: 0 1px 4px rgba(43,87,154,0.03);
            display: flex;
            align-items: center;
            gap: 8px;
            outline: none;
            cursor: pointer;
        }
        .toolbar-btn.active,
        .toolbar-btn:hover,
        .toolbar-btn:focus {
            border-color: #2b579a;
            background: #e8f1fb;
            color: #203864;
            box-shadow: 0 2px 8px rgba(43,87,154,0.09);
        }
    </style>
</head>

<body>

    <div class="header">
        <div class="header-top">
            <div><i class="bi bi-shield-lock-fill"></i> سیستم مدیریت مشتری Professional v1.0</div>
            <div><i class="bi bi-calendar-event"></i> امروز: شنبه 28 مهر 1403 | <i class="bi bi-clock"></i> 14:30</div>
        </div>
        <div class="header-main">
            <div class="logo">
                <i class="bi bi-people-fill"></i>
                <span>مدیریت حرفه ای مشتری</span>
            </div>
            <div class="user-info">
                <div>
                    <div class="d-flex align-items-center gap-2">
                        <div class="dropdown">
                            <button class="btn btn-white border-0 p-1 px-2 dropdown-toggle d-flex align-items-center gap-2" style="box-shadow:none;" type="button" id="userDropdown" data-bs-toggle="dropdown" aria-expanded="false">
                                <span class="d-flex flex-column align-items-start" style="line-height:1;">
                                    <span style="color:#fff; font-size:12px">سعید محمدی</span>
                                    <span class="text-muted" style="font-size:12px">مدیر سیستم</span>
                                </span>
                            </button>
                            <ul class="dropdown-menu dropdown-menu-start text-start" aria-labelledby="userDropdown">
                                <li><a class="dropdown-item" href="#"><i class="bi bi-gear me-2"></i>تنظیمات</a></li>
                                <li><hr class="dropdown-divider"></li>
                                <li><a class="dropdown-item text-danger" href="#"><i class="bi bi-box-arrow-right me-2"></i>خروج</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>


<div class="ribbon">
    <nav class="word-toolbar d-flex gap-2 py-2 px-3 justify-content-start" style="background:#f6f8fb; border-bottom:1.5px solid #d3e2f7;">
        <button class="toolbar-btn flex-column">
            <i class="bi bi-house-door"></i>
            <span>خانه</span>
        </button>
        <button class="toolbar-btn flex-column">
            <i class="bi bi-people"></i>
            <span>مشتریان</span>
        </button>
        <button class="toolbar-btn flex-column">
            <i class="bi bi-briefcase"></i>
            <span>پروژه‌ها</span>
        </button>
        <button class="toolbar-btn flex-column">
            <i class="bi bi-envelope"></i>
            <span>پیام‌ها</span>
        </button>
        <button class="toolbar-btn flex-column">
            <i class="bi bi-gear"></i>
            <span>تنظیمات</span>
        </button>
    </nav>
</div>


<div class="container-fluid mt-3">
    <div class="card shadow-sm border-0 rounded-4">
        <div class="card-header text-dark rounded-top-4 d-flex align-items-center justify-content-between">
            <h6 class="mb-0">
                <i class="bi bi-people-fill me-2"></i> لیست مشتریان
            </h6>
                <span class="badge bg-primary text-white px-3 py-1">۱۲ نفر</span>
            </div>
            <div class="card-body">
                <h6 class="card-subtitle mb-3 text-muted">اطلاعات مربوط به مشتریان ثبت‌شده</h6>
                <p class="card-text">شما می‌توانید در این بخش مشتریان جدید ثبت کنید، یا اطلاعات مشتریان قبلی را مشاهده و ویرایش نمایید.</p>
                <a href="#" class="btn btn-outline-primary">
                    <i class="bi bi-person-plus-fill me-1"></i> افزودن مشتری جدید
                </a>
            </div>
        </div>
    </div>
</div>

    <!-- Footer -->
    <footer class="footer mt-5">
        <div>طراحی و توسعه <a href="https://www.atlasm.ir" target="_blank">ونداد ارتباط بختگان</a></div>
    </footer>

    <script>
        function updateDateTime() {
            const now = new Date();
            const options = { day: 'numeric', month: 'long', year: 'numeric' };
            const time = now.toLocaleTimeString('fa-IR');
            const date = now.toLocaleDateString('fa-IR', options);
            document.getElementById("datetime").innerText = date + " - " + time;
        }
        setInterval(updateDateTime, 1000);
        updateDateTime();
    </script>
</body>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</html>
