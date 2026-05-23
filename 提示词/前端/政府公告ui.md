# 政府公告ui
```
整体风格
主题：政务公告 + 高级企业公告
基调：严肃正式、权威可信
配色：
主色：深蓝色（#003366 或 #002B5C，象征权威和稳重）
辅助色：白色背景（#FFFFFF），干净简洁
点缀色：浅灰色（#F5F5F5 或 #E6E6E6，用于分割线或表格背景）
版式设计
排版风格：

极简设计，留白充足，避免过多装饰元素。
强信息层级，突出标题、重点内容和数据表格。
使用现代UI风格，注重清晰性和易读性。
信息层级：

大标题：居中，使用深蓝色，字体加粗，字号明显（如 48px 或更大）。
副标题：位于标题下方，字体稍小，适合放置公告时间、主题等信息。
正文内容：左对齐，分段清晰，每段之间有适当间距。
表格区域：位于正文下方，用于展示数据，表格线条简洁，保持对齐。
对齐方式：

所有内容以网格系统对齐，保证视觉整洁。
标题居中，正文左对齐。
内容结构
企业LOGO：

放置于海报顶部中央或左上角，LOGO下方可加上企业名称。
LOGO大小适中，不抢占过多视觉焦点。
标题：

文字示例：《关于XX事项的通知》
居中放置，字体加粗，深蓝色。
副标题：

示例：2023年10月10日发布
使用浅灰色或深蓝色，字体稍小，位于标题正下方。
正文内容：

示例：“根据相关政策规定，现对XX事项进行公示如下……”
左对齐，使用标准字体（如思源黑体、微软雅黑等），字号适中（如 16px - 18px）。
表格展示：

表格示例：
┌─────────────┬─────────────┬─────────────┐
│ 数据类别      │ 数据内容      │ 更新时间      │
├─────────────┼─────────────┼─────────────┤
│ 示例数据1     │ 示例内容1     │ 2023-10-10   │
│ 示例数据2     │ 示例内容2     │ 2023-10-11   │
└─────────────┴─────────────┴─────────────┘
表格线条使用浅灰色，表头加粗或使用深蓝色背景，字体对齐整齐。
底部区域：

放置企业地址、联系方式、二维码（如有需要）。
使用浅灰色字体，字号较小，不抢占视觉焦点。
字体选择
标题字体：思源黑体、苹方、微软雅黑（加粗）
正文字体：思源黑体、苹方、微软雅黑（常规）
字号建议：标题 48px、副标题 24px、正文 16px、表格 14px
设计要点
权威性：

深蓝色搭配白色背景，传递正式感。
留白处理，避免杂乱，突出信息核心。
现代感：

使用扁平化设计，表格和图表风格简洁。
使用轻微的阴影或渐变点缀，避免单调。
信息清晰性：

强调标题和重点内容，使用加粗和字号区分。
表格对齐，数据清晰。
最终效果
一张干净、权威、可信的公告海报，适合金融科技、政务或B端产品相关的正式通知场景。
```
```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>政务公告</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-blue: #002B5C;
            --deep-blue: #003366;
            --white: #FFFFFF;
            --light-gray-bg: #F5F5F5;
            --border-gray: #E6E6E6;
            --text-dark: #333333;
            --text-secondary: #666666;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: "Source Han Sans SC", "Noto Sans SC", "PingFang SC", "Microsoft YaHei", sans-serif;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 40px 20px;
        }

        .poster-container {
            width: 100%;
            max-width: 900px;
            background: var(--white);
            box-shadow: 0 25px 80px rgba(0, 43, 92, 0.12), 0 8px 30px rgba(0, 43, 92, 0.08);
            border-radius: 4px;
            overflow: hidden;
            animation: fadeInUp 0.6s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .poster-content {
            padding: 60px 80px;
        }

        /* Logo 区域 */
        .logo-section {
            text-align: center;
            margin-bottom: 40px;
        }

        .logo-wrapper {
            display: inline-flex;
            align-items: center;
            gap: 16px;
        }

        .logo-icon {
            width: 56px;
            height: 56px;
            background: linear-gradient(135deg, var(--primary-blue) 0%, var(--deep-blue) 100%);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 12px rgba(0, 43, 92, 0.25);
        }

        .logo-icon svg {
            width: 32px;
            height: 32px;
            fill: var(--white);
        }

        .logo-text {
            font-size: 26px;
            font-weight: 700;
            color: var(--primary-blue);
            letter-spacing: 3px;
        }

        /* 装饰线 */
        .decorative-line {
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--primary-blue) 20%, var(--primary-blue) 80%, transparent);
            margin: 0 auto 40px;
            max-width: 600px;
            border-radius: 2px;
        }

        /* 主标题 */
        .main-title {
            text-align: center;
            font-size: 42px;
            font-weight: 700;
            color: var(--primary-blue);
            letter-spacing: 4px;
            margin-bottom: 20px;
            line-height: 1.4;
        }

        .title-brackets {
            color: var(--deep-blue);
            opacity: 0.6;
        }

        /* 发布日期 */
        .publish-date {
            text-align: center;
            font-size: 17px;
            color: var(--text-secondary);
            margin-bottom: 36px;
            letter-spacing: 2px;
        }

        /* 正文内容 */
        .content-section {
            margin-bottom: 44px;
        }

        .content-paragraph {
            font-size: 17px;
            line-height: 2.2;
            color: var(--text-dark);
            text-align: justify;
            letter-spacing: 1px;
            margin-bottom: 20px;
            text-indent: 2em;
        }

        .content-paragraph:last-child {
            margin-bottom: 0;
        }

        /* 关键词高亮 */
        .highlight {
            color: var(--primary-blue);
            font-weight: 500;
        }

        /* 表格区域 */
        .table-section {
            margin-bottom: 44px;
        }

        .table-wrapper {
            overflow-x: auto;
            border-radius: 8px;
            box-shadow: 0 2px 12px rgba(0, 43, 92, 0.08);
        }

        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 15px;
        }

        thead th {
            background: linear-gradient(135deg, var(--deep-blue) 0%, var(--primary-blue) 100%);
            color: var(--white);
            font-weight: 500;
            padding: 16px 20px;
            text-align: left;
            letter-spacing: 1px;
            white-space: nowrap;
        }

        thead th:first-child {
            border-top-left-radius: 8px;
        }

        thead th:last-child {
            border-top-right-radius: 8px;
        }

        tbody tr {
            transition: background-color 0.2s ease;
        }

        tbody tr:nth-child(odd) {
            background-color: var(--light-gray-bg);
        }

        tbody tr:nth-child(even) {
            background-color: var(--white);
        }

        tbody tr:hover {
            background-color: rgba(0, 43, 92, 0.04);
        }

        tbody td {
            padding: 14px 20px;
            color: var(--text-dark);
            border-bottom: 1px solid var(--border-gray);
        }

        tbody tr:last-child td {
            border-bottom: none;
        }

        tbody tr:last-child td:first-child {
            border-bottom-left-radius: 8px;
        }

        tbody tr:last-child td:last-child {
            border-bottom-right-radius: 8px;
        }

        /* 底部区域 */
        .bottom-line {
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--border-gray) 20%, var(--border-gray) 80%, transparent);
            margin-bottom: 32px;
        }

        .footer-section {
            text-align: center;
        }

        .footer-info {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 24px;
            flex-wrap: wrap;
            font-size: 14px;
            color: var(--text-secondary);
            letter-spacing: 1px;
        }

        .footer-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .footer-item svg {
            width: 16px;
            height: 16px;
            fill: var(--primary-blue);
            opacity: 0.7;
        }

        .separator {
            color: var(--border-gray);
        }

        .qr-code {
            width: 64px;
            height: 64px;
            background: var(--light-gray-bg);
            border-radius: 6px;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 6px;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            cursor: pointer;
        }

        .qr-code:hover {
            transform: scale(1.08);
            box-shadow: 0 4px 16px rgba(0, 43, 92, 0.15);
        }

        .qr-code svg {
            width: 100%;
            height: 100%;
        }

        .copyright {
            margin-top: 20px;
            font-size: 12px;
            color: #999999;
            letter-spacing: 1px;
        }

        /* 权威标识 */
        .authority-badge {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: rgba(0, 43, 92, 0.06);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 13px;
            color: var(--primary-blue);
            margin-top: 24px;
        }

        .authority-badge svg {
            width: 14px;
            height: 14px;
            fill: var(--primary-blue);
        }

        /* 响应式 */
        @media (max-width: 768px) {
            .poster-content {
                padding: 40px 28px;
            }

            .main-title {
                font-size: 28px;
                letter-spacing: 2px;
            }

            .logo-text {
                font-size: 20px;
                letter-spacing: 2px;
            }

            .content-paragraph {
                font-size: 15px;
                line-height: 2;
                text-align: left;
            }

            .footer-info {
                flex-direction: column;
                gap: 12px;
            }

            .separator {
                display: none;
            }
        }

        /* 打印样式 */
        @media print {
            body {
                background: white;
                padding: 0;
            }

            .poster-container {
                box-shadow: none;
                max-width: 100%;
            }
        }
    </style>
</head>
<body>
    <article class="poster-container">
        <div class="poster-content">
            <!-- Logo 区域 -->
            <header class="logo-section">
                <div class="logo-wrapper">
                    <div class="logo-icon">
                        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/>
                        </svg>
                    </div>
                    <span class="logo-text">智慧政务服务中心</span>
                </div>
            </header>

            <!-- 装饰线 -->
            <div class="decorative-line"></div>

            <!-- 主标题 -->
            <h1 class="main-title">
                <span class="title-brackets">《</span>关于规范数据安全管理事项的通知<span class="title-brackets">》</span>
            </h1>

            <!-- 发布日期 -->
            <p class="publish-date">二〇二六年五月二十三日发布</p>

            <!-- 正文内容 -->
            <section class="content-section">
                <p class="content-paragraph">
                    各相关单位、企业及个人：<br><br>
                    为深入贯彻落实《数据安全法》《个人信息保护法》等法律法规要求，进一步加强<span class="highlight">数据安全管理</span>，规范数据处理活动，保障数据安全，促进数据开发利用，现将有关事项通知如下。
                </p>
                <p class="content-paragraph">
                    各单位应严格落实数据安全主体责任，建立健全数据安全管理制度，完善数据分类分级保护机制，加强重要数据和个人信息的<span class="highlight">保护措施</span>，确保数据全生命周期安全可控。
                </p>
                <p class="content-paragraph">
                    请各相关单位按照要求，认真组织开展数据安全自查自纠工作，并于规定时限内完成整改。现将<span class="highlight">数据安全管理规范要点</span>公示如下，请知悉并严格执行。
                </p>
            </section>

            <!-- 数据表格 -->
            <section class="table-section">
                <div class="table-wrapper">
                    <table>
                        <thead>
                            <tr>
                                <th>序号</th>
                                <th>管理类别</th>
                                <th>具体要求</th>
                                <th>执行期限</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>01</td>
                                <td>制度建设</td>
                                <td>建立完善的数据安全管理制度和应急预案</td>
                                <td>30日内</td>
                            </tr>
                            <tr>
                                <td>02</td>
                                <td>分类分级</td>
                                <td>完成数据资产梳理与分类分级标注工作</td>
                                <td>45日内</td>
                            </tr>
                            <tr>
                                <td>03</td>
                                <td>权限管理</td>
                                <td>实施最小权限原则，完善访问控制机制</td>
                                <td>15日内</td>
                            </tr>
                            <tr>
                                <td>04</td>
                                <td>加密防护</td>
                                <td>对重要数据实施加密存储与传输保护</td>
                                <td>60日内</td>
                            </tr>
                            <tr>
                                <td>05</td>
                                <td>审计监控</td>
                                <td>部署数据安全审计与实时监控系统</td>
                                <td>90日内</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </section>

            <!-- 底部装饰线 -->
            <div class="bottom-line"></div>

            <!-- 底部信息 -->
            <footer class="footer-section">
                <div class="footer-info">
                    <div class="footer-item">
                        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/>
                        </svg>
                        <span>北京市海淀区中关村大街1号</span>
                    </div>
                    <span class="separator">|</span>
                    <div class="footer-item">
                        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/>
                        </svg>
                        <span>010-8888-6666</span>
                    </div>
                    <span class="separator">|</span>
                    <div class="qr-code" title="扫描关注官方公众号">
                        <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg">
                            <rect x="4" y="4" width="24" height="24" fill="#002B5C"/>
                            <rect x="8" y="8" width="16" height="16" fill="#FFFFFF"/>
                            <rect x="12" y="12" width="8" height="8" fill="#002B5C"/>
                            <rect x="36" y="4" width="24" height="24" fill="#002B5C"/>
                            <rect x="40" y="8" width="16" height="16" fill="#FFFFFF"/>
                            <rect x="44" y="12" width="8" height="8" fill="#002B5C"/>
                            <rect x="4" y="36" width="24" height="24" fill="#002B5C"/>
                            <rect x="8" y="40" width="16" height="16" fill="#FFFFFF"/>
                            <rect x="12" y="44" width="8" height="8" fill="#002B5C"/>
                            <rect x="36" y="36" width="4" height="4" fill="#002B5C"/>
                            <rect x="42" y="36" width="4" height="4" fill="#002B5C"/>
                            <rect x="48" y="36" width="4" height="4" fill="#002B5C"/>
                            <rect x="54" y="36" width="6" height="4" fill="#002B5C"/>
                            <rect x="36" y="42" width="4" height="4" fill="#002B5C"/>
                            <rect x="48" y="42" width="4" height="4" fill="#002B5C"/>
                            <rect x="36" y="48" width="4" height="4" fill="#002B5C"/>
                            <rect x="42" y="48" width="6" height="4" fill="#002B5C"/>
                            <rect x="54" y="48" width="6" height="4" fill="#002B5C"/>
                            <rect x="36" y="54" width="4" height="6" fill="#002B5C"/>
                            <rect x="42" y="54" width="4" height="6" fill="#002B5C"/>
                            <rect x="48" y="54" width="4" height="6" fill="#002B5C"/>
                        </svg>
                    </div>
                </div>
                <div class="authority-badge">
                    <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 1L3 5v6c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V5l-9-4zm0 10.99h7c-.53 4.12-3.28 7.79-7 8.94V12H5V6.3l7-3.11v8.8z"/>
                    </svg>
                    <span>官方认证 · 权威发布</span>
                </div>
                <p class="copyright">智慧政务服务中心 © 2026 版权所有</p>
            </footer>
        </div>
    </article>
</body>
</html>
```
