AI: deepseek

lệng dùng: 



thêm css vào dòng code trên và không can thiệp thay đổi html

kết quả



<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title> giao diện apple rep 1:1 </title>
    <style>
        /* ---------- RESET & GLOBAL (Apple style base) ---------- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #ffffff;
            font-family: -apple-system, 'SF Pro Text', 'SF Pro Icons', 'Helvetica Neue', Helvetica, Arial, sans-serif;
            color: #1d1c1e;
            line-height: 1.42859;
            letter-spacing: -0.016em;
            -webkit-font-smoothing: antialiased;
        }

        /* container style cho toàn bộ layout – giữ các block căn giữa tự nhiên */
        body>div {
            max-width: 1200px;
            margin-left: auto;
            margin-right: auto;
            padding-left: 22px;
            padding-right: 22px;
        }

        /* ---------- QUỐC GIA / REGION BANNER (Apple-style notification) ---------- */
        #QuocGia {
            background-color: #f5f5f7;
            border-radius: 18px;
            margin-top: 20px;
            margin-bottom: 20px;
            padding: 14px 24px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 12px 20px;
            font-size: 14px;
            font-weight: 400;
            color: #1d1c1e;
            backdrop-filter: blur(0px);
            box-shadow: 0 1px 0 rgba(0, 0, 0, 0.02), inset 0 1px 0 rgba(255, 255, 255, 0.6);
            border: 0.5px solid rgba(0, 0, 0, 0.04);
        }

        #QuocGia p {
            margin: 0;
            font-size: 14px;
            color: #1d1c1e;
            flex: 2 1 240px;
        }

        #QuocGia select {
            background-color: #ffffff;
            border: 1px solid #d2d2d7;
            border-radius: 12px;
            padding: 8px 32px 8px 16px;
            font-size: 14px;
            font-family: inherit;
            color: #1d1c1e;
            appearance: none;
            background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23686868' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'><polyline points='6 9 12 15 18 9'></polyline></svg>");
            background-repeat: no-repeat;
            background-position: right 12px center;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        #QuocGia select:hover {
            border-color: #86868b;
        }

        #QuocGia select:focus {
            outline: none;
            border-color: #0071e3;
            box-shadow: 0 0 0 3px rgba(0, 113, 227, 0.2);
        }

        #QuocGia button {
            background-color: #0071e3;
            border: none;
            border-radius: 980px;
            padding: 7px 21px;
            font-size: 14px;
            font-weight: 500;
            font-family: inherit;
            color: white;
            cursor: pointer;
            transition: all 0.2s ease;
            letter-spacing: -0.01em;
        }

        #QuocGia button:hover {
            background-color: #005fc5;
            transform: scale(0.98);
        }

        #QuocGia a[title="Đóng"] {
            font-size: 26px;
            font-weight: 300;
            line-height: 1;
            color: #8e8e93;
            text-decoration: none;
            background-color: #e8e8ed;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s ease;
            cursor: pointer;
            margin-left: 4px;
        }

        #QuocGia a[title="Đóng"]:hover {
            background-color: #d2d2d7;
            color: #1d1c1e;
            transform: scale(1.02);
        }

        /* ---------- NAVIGATION BAR (Apple global nav style) ---------- */
        #navigation {
            background-color: rgba(255, 255, 255, 0.96);
            backdrop-filter: blur(20px);
            border-radius: 32px;
            margin: 12px 0 28px 0;
            padding: 6px 18px;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: center;
            gap: 8px 22px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.02), 0 1px 0 rgba(0, 0, 0, 0.02);
            border-bottom: 0.5px solid rgba(0, 0, 0, 0.06);
        }

        #navigation a {
            font-size: 14px;
            font-weight: 500;
            color: #1d1c1e;
            text-decoration: none;
            letter-spacing: -0.01em;
            cursor: pointer;
            transition: color 0.2s ease;
            padding: 6px 0;
            white-space: nowrap;
        }

        #navigation a:hover {
            color: #0071e3;
        }

        /* Apple logo and search/bag icons slightly bigger */
        #navigation a:first-child {
            font-size: 22px;
            font-weight: 400;
            margin-right: 2px;
        }

        #navigation a:nth-last-child(2),
        #navigation a:last-child {
            font-size: 18px;
            font-weight: 400;
        }

        /* responsive nav: scroll on small screens if needed */
        @media (max-width: 780px) {
            #navigation {
                overflow-x: auto;
                justify-content: flex-start;
                flex-wrap: nowrap;
                -webkit-overflow-scrolling: touch;
                scrollbar-width: thin;
                border-radius: 28px;
                gap: 18px;
            }

            #navigation a {
                white-space: nowrap;
            }

            body>div {
                padding-left: 18px;
                padding-right: 18px;
            }
        }

        /* ---------- PRODUCT SECTION (MacBook Neo) – Apple hero style ---------- */
        /* target the third div (product container) without modifying HTML */
        body>div:last-of-type {
            margin-top: 20px;
            margin-bottom: 64px;
            overflow: auto;
            /* clearfix for floated image */
            position: relative;
            padding-top: 20px;
            padding-bottom: 40px;
        }

        /* image float right = classic two-column Apple look */
        body>div:last-of-type img {
            float: right;
            width: 52%;
            max-width: 580px;
            margin-left: 40px;
            margin-bottom: 20px;
            border-radius: 28px;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.15), 0 0 0 0.5px rgba(0, 0, 0, 0.02);
            transition: transform 0.3s ease;
        }

        body>div:last-of-type img:hover {
            transform: scale(1.01);
        }

        /* heading & text styling */
        body>div:last-of-type h1 {
            font-size: 52px;
            font-weight: 700;
            letter-spacing: -0.003em;
            background: linear-gradient(135deg, #1c1c1e, #3a3a3e);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            margin-top: 28px;
            margin-bottom: 12px;
            line-height: 1.07143;
        }

        body>div:last-of-type h2 {
            font-size: 26px;
            font-weight: 500;
            color: #6e6e73;
            letter-spacing: -0.008em;
            margin-bottom: 28px;
            line-height: 1.2;
        }

        /* two buttons inline like Apple CTA group */
        body>div:last-of-type button {
            background: transparent;
            border: none;
            font-family: inherit;
            font-size: 17px;
            font-weight: 500;
            padding: 12px 24px;
            border-radius: 980px;
            cursor: pointer;
            transition: all 0.25s cubic-bezier(0.25, 0.1, 0.25, 1);
            margin-right: 16px;
            margin-bottom: 12px;
            display: inline-block;
        }

        /* "Learn more" button outline style */
        body>div:last-of-type button:first-of-type {
            background-color: transparent;
            border: 1px solid #0071e3;
            color: #0071e3;
        }

        body>div:last-of-type button:first-of-type:hover {
            background-color: #0071e3;
            color: white;
            box-shadow: 0 8px 18px rgba(0, 113, 227, 0.2);
            transform: scale(0.98);
        }

        /* "Buy" button filled Apple blue */
        body>div:last-of-type button:last-of-type {
            background-color: #0071e3;
            color: white;
            border: none;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
        }

        body>div:last-of-type button:last-of-type:hover {
            background-color: #005bb5;
            transform: scale(0.98);
            box-shadow: 0 8px 20px rgba(0, 113, 227, 0.25);
        }

        /* empty paragraph (no content) – hide to avoid extra spacing */
        body>div:last-of-type p:empty {
            display: none;
        }

        /* optional spacing for any non-empty p (none here) but keep safety */
        body>div:last-of-type p:not(:empty) {
            margin-top: 20px;
            font-size: 15px;
            color: #515154;
        }

        /* Responsive: on medium screens, reduce image width and heading */
        @media (max-width: 900px) {
            body>div:last-of-type img {
                width: 45%;
                margin-left: 28px;
            }

            body>div:last-of-type h1 {
                font-size: 42px;
            }

            body>div:last-of-type h2 {
                font-size: 22px;
            }
        }

        /* Mobile: float none, full width image below text */
        @media (max-width: 680px) {
            body>div:last-of-type img {
                float: none;
                width: 100%;
                margin-left: 0;
                margin-top: 32px;
                display: block;
            }

            body>div:last-of-type h1 {
                font-size: 36px;
            }

            body>div:last-of-type h2 {
                font-size: 20px;
            }

            body>div:last-of-type button {
                display: inline-block;
                margin-right: 12px;
                padding: 10px 20px;
                font-size: 15px;
            }

            #QuocGia {
                flex-direction: column;
                align-items: stretch;
                text-align: center;
            }

            #QuocGia a[title="Đóng"] {
                align-self: flex-end;
            }
        }

        /* subtle global improvements */
        a,
        button {
            cursor: pointer;
        }

        /* inherit proper button reset */
        button {
            background: none;
            border: none;
        }

        /* improve spacing between sections */
        #navigation+div {
            margin-top: 0;
        }

        /* enhance focus ring for accessibility */
        button:focus-visible,
        select:focus-visible,
        a:focus-visible {
            outline: 2px solid #0071e3;
            outline-offset: 2px;
            border-radius: 6px;
        }
    </style>
</head>

<body>

    <div id="QuocGia" align="center">

        <p>
            Chọn quốc gia hoặc khu vực khác để xem nội dung dành riêng cho vị trí của bạn và mua sắm trực tuyến.
        </p>

        <select>
            <option>Việt Nam</option>
            <option>United States</option>
            <option>Japan</option>
        </select>

        <button>Tiếp Tục</button>

        <a title="Đóng">&times;</a>

    </div>


    <div id="navigation" align="center">

        <a>🍎</a>
        <a>Store</a>
        <a>Mac</a>
        <a>iPad</a>
        <a>iPhone</a>
        <a>Watch</a>
        <a>Vision</a>
        <a>AirPods</a>
        <a>TV & Home</a>
        <a>Entertainment</a>
        <a>Accessories</a>
        <a>Support</a>
        <a>🔍</a>
        <a>🛒</a>

    </div>
    <div>

        <h1>MacBook Neo</h1>

        <h2>Amazing Mac. Surprising price.</h2>

        <button>Learn more</button>

        <button>Buy</button>

        <p></p>

        <img src="https://store.storeimages.cdn-apple.com/1/as-images.apple.com/is/macbook-neo-color-unselect-202603-gallery-1?wid=5120&hei=3280&fmt=webp&qlt=90&.v=TytZbDBUUnRqRElRcFlBSHpmZVVDK3BoR2lIdGdhMDNQSUZrOHIycWd6Vmd1bjBBbHBBMFNjNjVIN0pUcUg2U0tZMGFKbG9yanhQdjZDS1dZUFFhRVE4bm1RcmlWRWp2eDN1WHNkSjNmUmFub3B6RFdCcnJtSHE1TzBCb3pCcis&traceId=1"
            alt="MacBook Neo">

    </div>


</body>

</html>
