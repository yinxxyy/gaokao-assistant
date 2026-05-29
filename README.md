<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>志翼翱翔 - 霍兰德职业兴趣测试与高考专业推荐</title>
    <style>
        :root {
            --primary: #4f46e5;
            --primary-dark: #3730a3;
            --primary-light: #eef2ff;
            --success: #059669;
            --warning: #d97706;
            --danger: #dc2626;
            --bg: #f1f5f9;
            --card-bg: #ffffff;
            --text: #1e293b;
            --text-secondary: #64748b;
            --border: #e2e8f0;
            --shadow-sm: 0 1px 2px rgba(0,0,0,0.05);
            --shadow: 0 1px 3px rgba(0,0,0,0.06), 0 1px 2px rgba(0,0,0,0.04);
            --shadow-md: 0 4px 6px rgba(0,0,0,0.07), 0 2px 4px rgba(0,0,0,0.06);
            --shadow-lg: 0 10px 25px rgba(0,0,0,0.1), 0 4px 10px rgba(0,0,0,0.06);
            --radius: 16px;
            --radius-sm: 10px;
        }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Microsoft YaHei', sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.7;
            min-height: 100vh;
        }
        .header {
            background: linear-gradient(135deg, #312e81 0%, #4f46e5 40%, #7c3aed 100%);
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 24px rgba(79,70,229,0.3);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
        }
        .header-inner {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 24px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 14px;
        }
        .header .logo {
            font-size: 1.55rem;
            font-weight: 800;
            letter-spacing: 2px;
            background: linear-gradient(90deg, #fbbf24, #fde68a);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .header .logo span { -webkit-text-fill-color: #fbbf24; }
        .header .subtitle { font-size: 0.85rem; opacity: 0.8; margin-top: 2px; }
        .nav-links { display: flex; gap: 6px; flex-wrap: wrap; }
        .nav-btn {
            padding: 9px 20px;
            border-radius: 22px;
            border: 1.5px solid rgba(255,255,255,0.2);
            background: rgba(255,255,255,0.08);
            color: white;
            cursor: pointer;
            font-size: 0.88rem;
            transition: all 0.3s cubic-bezier(0.4,0,0.2,1);
            font-weight: 500;
            position: relative;
            overflow: hidden;
        }
        .nav-btn::before {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(135deg, rgba(255,255,255,0.15), transparent);
            opacity: 0;
            transition: opacity 0.3s;
        }
        .nav-btn:hover::before { opacity: 1; }
        .nav-btn:hover { background: rgba(255,255,255,0.2); border-color: rgba(255,255,255,0.5); transform: translateY(-1px); }
        .nav-btn.active {
            background: white;
            color: #4f46e5;
            border-color: white;
            font-weight: 700;
            box-shadow: 0 2px 12px rgba(0,0,0,0.15);
        }
        .container { max-width: 1000px; margin: 0 auto; padding: 36px 20px 60px; }
        .page { display: none; }
        .page.active { display: block; animation: fadeIn 0.4s cubic-bezier(0.4,0,0.2,1); }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(16px); } to { opacity: 1; transform: translateY(0); } }
        .card {
            background: var(--card-bg);
            border-radius: var(--radius);
            padding: 32px 36px;
            margin-bottom: 20px;
            box-shadow: var(--shadow-md);
            border: 1px solid var(--border);
            transition: box-shadow 0.3s;
        }
        .card:hover { box-shadow: var(--shadow-lg); }
        .card h2 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: #312e81;
            display: flex;
            align-items: center;
            gap: 10px;
            padding-bottom: 12px;
            border-bottom: 2px solid var(--primary-light);
        }
        .card h3 { font-size: 1.08rem; margin-bottom: 12px; color: #334155; }
        .card-intro {
            background: linear-gradient(135deg, #eef2ff 0%, #e0e7ff 100%);
            border: 1px solid #c7d2fe;
            border-radius: var(--radius);
            padding: 28px 32px;
            margin-bottom: 20px;
            text-align: center;
        }
        .card-intro h2 { color: #3730a3; border-bottom-color: #c7d2fe; }
        .dl-icon {
            width: 52px; height: 52px;
            border-radius: 14px;
            display: flex; align-items: center; justify-content: center;
            font-size: 0.85rem; font-weight: 700;
            color: white; margin-bottom: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
        }
        .dl-icon.school { background: linear-gradient(135deg, #f59e0b, #ea580c); }
        .dl-icon.student { background: linear-gradient(135deg, #4f46e5, #3b82f6); }
        .dl-icon.shandong { background: linear-gradient(135deg, #10b981, #059669); }
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            padding: 11px 26px;
            border-radius: 26px;
            border: none;
            font-size: 0.93rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.4,0,0.2,1);
            text-decoration: none;
            letter-spacing: 0.3px;
        }
        .btn-primary {
            background: linear-gradient(135deg, #4f46e5, #6366f1);
            color: white;
            box-shadow: 0 4px 14px rgba(79,70,229,0.3);
        }
        .btn-primary:hover:not(:disabled) { background: linear-gradient(135deg, #4338ca, #4f46e5); transform: translateY(-2px); box-shadow: 0 6px 20px rgba(79,70,229,0.4); }
        .btn-primary:disabled { opacity: 0.5; cursor: not-allowed; }
        .btn-success {
            background: linear-gradient(135deg, #059669, #10b981);
            color: white;
            box-shadow: 0 4px 14px rgba(5,150,105,0.3);
        }
        .btn-success:hover { background: linear-gradient(135deg, #047857, #059669); transform: translateY(-2px); box-shadow: 0 6px 20px rgba(5,150,105,0.4); }
        .btn-outline {
            background: white;
            color: #4f46e5;
            border: 2px solid #4f46e5;
            box-shadow: var(--shadow-sm);
        }
        .btn-outline:hover { background: #eef2ff; border-color: #4338ca; color: #4338ca; transform: translateY(-1px); }
        .btn-sm { padding: 7px 18px; font-size: 0.82rem; border-radius: 20px; }
        .btn-lg { padding: 15px 38px; font-size: 1.08rem; border-radius: 30px; }
        .progress-wrap { padding: 8px 0; }
        .progress-bar { height: 10px; background: #e2e8f0; border-radius: 10px; margin: 20px 0 10px; overflow: hidden; }
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #4f46e5, #7c3aed, #a78bfa);
            border-radius: 10px;
            transition: width 0.6s cubic-bezier(0.4,0,0.2,1);
            box-shadow: 0 0 12px rgba(79,70,229,0.35);
        }
        .question-block {
            background: #f8fafc;
            border-radius: var(--radius-sm);
            padding: 22px 26px;
            margin-bottom: 14px;
            border-left: 4px solid var(--primary);
            transition: all 0.25s;
        }
        .question-block:hover { background: #f1f5f9; box-shadow: var(--shadow-sm); }
        .question-text { font-size: 1.02rem; font-weight: 500; margin-bottom: 14px; color: #334155; }
        .options { display: flex; gap: 10px; flex-wrap: wrap; }
        .option-btn {
            padding: 9px 22px;
            border-radius: 22px;
            border: 2px solid #d1d5db;
            background: white;
            cursor: pointer;
            font-size: 0.88rem;
            transition: all 0.25s;
            color: #4b5563;
            font-weight: 500;
        }
        .option-btn:hover { border-color: #818cf8; color: #4f46e5; background: #eef2ff; transform: translateY(-1px); }
        .option-btn.selected { background: linear-gradient(135deg, #4f46e5, #6366f1); color: white; border-color: transparent; font-weight: 700; box-shadow: 0 2px 8px rgba(79,70,229,0.3); }
        .type-card {
            background: linear-gradient(135deg, #f0f9ff, #e0f2fe);
            border-radius: var(--radius);
            padding: 20px 24px;
            margin-bottom: 12px;
            border: 1px solid #bae6fd;
            transition: all 0.3s;
        }
        .type-card.high {
            background: linear-gradient(135deg, #ecfdf5, #d1fae5);
            border-color: #6ee7b7;
            box-shadow: 0 0 0 2px rgba(5,150,105,0.1);
        }
        .type-bar { height: 30px; background: #e2e8f0; border-radius: 15px; overflow: hidden; margin: 8px 0; }
        .type-bar-fill {
            height: 100%;
            border-radius: 15px;
            transition: width 0.9s cubic-bezier(0.4,0,0.2,1);
            display: flex;
            align-items: center;
            justify-content: flex-end;
            padding-right: 14px;
            color: white;
            font-weight: 700;
            font-size: 0.85rem;
            min-width: 40px;
        }
        .holland-code-badge {
            display: inline-flex;
            gap: 6px;
            margin: 10px 0;
        }
        .holland-code-badge span {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 44px; height: 44px;
            border-radius: 12px;
            font-size: 1.3rem;
            font-weight: 800;
            color: white;
            box-shadow: 0 2px 8px rgba(0,0,0,0.15);
        }
        .major-list { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 12px; }
        .major-item {
            background: #f8fafc;
            border-radius: var(--radius-sm);
            padding: 16px 20px;
            border: 1px solid var(--border);
            cursor: pointer;
            transition: all 0.25s;
            position: relative;
            overflow: hidden;
        }
        .major-item::after {
            content: '';
            position: absolute;
            top: 0; right: 0;
            width: 40px; height: 40px;
            background: var(--primary-light);
            border-radius: 0 0 0 40px;
            opacity: 0;
            transition: opacity 0.25s;
        }
        .major-item:hover::after { opacity: 1; }
        .major-item:hover {
            background: #eef2ff;
            border-color: #a5b4fc;
            transform: translateY(-3px);
            box-shadow: var(--shadow-md);
        }
        .major-item .major-name { font-weight: 600; color: #3730a3; font-size: 0.95rem; }
        .major-item .major-match { font-size: 0.82rem; color: var(--success); margin-top: 4px; font-weight: 600; }
        .download-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 18px; }
        .download-card {
            background: white;
            border-radius: var(--radius);
            padding: 24px 28px;
            border: 1px solid var(--border);
            transition: all 0.3s cubic-bezier(0.4,0,0.2,1);
            position: relative;
            overflow: hidden;
        }
        .download-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0;
            width: 100%; height: 4px;
            background: linear-gradient(90deg, #4f46e5, #7c3aed);
            opacity: 0;
            transition: opacity 0.3s;
        }
        .download-card:hover::before { opacity: 1; }
        .download-card:hover { transform: translateY(-4px); box-shadow: var(--shadow-lg); border-color: #c7d2fe; }
        .download-card h4 { font-size: 0.98rem; margin-bottom: 8px; color: #1e293b; }
        .download-card .desc { font-size: 0.85rem; color: #64748b; margin-bottom: 14px; }
        .xianyu-section { text-align: center; padding: 36px 24px; }
        .xianyu-section img {
            max-width: 240px;
            border-radius: 16px;
            box-shadow: 0 8px 30px rgba(0,0,0,0.12);
            margin: 20px 0;
            border: 3px solid #f1f5f9;
            transition: transform 0.3s;
        }
        .xianyu-section img:hover { transform: scale(1.02); }
        .xianyu-section .qr-hint {
            color: #dc2626;
            font-weight: 700;
            font-size: 1.05rem;
            margin: 8px 0;
            display: inline-block;
            padding: 6px 20px;
            background: #fef2f2;
            border-radius: 20px;
        }
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(15,23,42,0.6);
            backdrop-filter: blur(4px);
            z-index: 200;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        .modal-overlay.show { display: flex; animation: modalFadeIn 0.25s ease; }
        @keyframes modalFadeIn { from { opacity: 0; } to { opacity: 1; } }
        .modal {
            background: white;
            border-radius: var(--radius);
            max-width: 720px;
            width: 100%;
            max-height: 85vh;
            overflow-y: auto;
            padding: 36px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.2);
            position: relative;
            animation: modalSlideIn 0.3s cubic-bezier(0.4,0,0.2,1);
        }
        @keyframes modalSlideIn { from { transform: translateY(30px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        .modal-close {
            position: absolute;
            top: 16px; right: 20px;
            width: 36px; height: 36px;
            border-radius: 50%;
            font-size: 1.3rem;
            cursor: pointer;
            background: #f1f5f9;
            border: none;
            color: #64748b;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s;
        }
        .modal-close:hover { background: #e2e8f0; color: #1e293b; }
        .tabs { display: flex; gap: 4px; margin-bottom: 20px; border-bottom: 2px solid var(--border); flex-wrap: wrap; }
        .tab {
            padding: 10px 22px;
            cursor: pointer;
            border: none;
            background: none;
            font-size: 0.93rem;
            color: var(--text-secondary);
            border-bottom: 3px solid transparent;
            margin-bottom: -2px;
            transition: all 0.25s;
            font-weight: 500;
            border-radius: 8px 8px 0 0;
        }
        .tab:hover { color: #4f46e5; background: #f8fafc; }
        .tab.active { color: #4f46e5; border-bottom-color: #4f46e5; font-weight: 700; background: var(--primary-light); }
        .search-box { display: flex; gap: 10px; margin-bottom: 20px; }
        .search-box input {
            flex: 1;
            padding: 13px 20px;
            border: 2px solid var(--border);
            border-radius: 28px;
            font-size: 0.95rem;
            outline: none;
            transition: all 0.25s;
            background: #f8fafc;
        }
        .search-box input:focus { border-color: #4f46e5; background: white; box-shadow: 0 0 0 4px rgba(79,70,229,0.08); }
        .footer {
            text-align: center;
            padding: 28px;
            color: #94a3b8;
            font-size: 0.85rem;
            border-top: 1px solid var(--border);
            background: white;
        }
        .tag {
            display: inline-block;
            padding: 4px 12px;
            border-radius: 12px;
            font-size: 0.8rem;
            font-weight: 600;
        }
        .highlight-card {
            background: linear-gradient(135deg, #fefce8, #fffbeb);
            border: 1px solid #fde68a;
            border-radius: var(--radius);
            padding: 24px 28px;
            margin-bottom: 16px;
        }
        @media (max-width: 768px) {
            .header-inner { flex-direction: column; text-align: center; }
            .card { padding: 22px 18px; }
            .download-grid { grid-template-columns: 1fr; }
            .options { flex-direction: column; }
            .option-btn { text-align: center; }
            .modal { padding: 24px 18px; }
        }
        @media print {
            body { background: white; }
            .header, .nav-links, .btn, .modal-close, .footer { display: none !important; }
            .modal-overlay { position: static; display: block !important; }
            .modal { max-width: 100%; box-shadow: none; padding: 20px; }
        }
    </style>
</head>
<body>

<!-- Header -->
<div class="header">
    <div class="header-inner">
        <div>
            <div class="logo">志翼<span>翱翔</span></div>
            <div class="subtitle">霍兰德职业兴趣测试 · 高考专业推荐</div>
        </div>
        <div class="nav-links">
            <button class="nav-btn active" onclick="showPage('test', this)">兴趣测试</button>
            <button class="nav-btn" onclick="showPage('result', this)" id="nav-result">测试结果</button>
            <button class="nav-btn" onclick="showPage('majors', this)">专业查询</button>
            <button class="nav-btn" onclick="showPage('hotMajors', this)">热门专业</button>
            <button class="nav-btn" onclick="showPage('download', this)">系统下载</button>
        </div>
    </div>
</div>

<div class="container">

    <!-- ========== 测试页面 ========== -->
    <div class="page active" id="page-test">
        <div class="card-intro">
            <h2>霍兰德职业兴趣测试 (SDS)</h2>
            <p style="color:#475569;margin-bottom:16px;font-size:0.95rem;">
                由美国心理学家约翰·霍兰德提出，将人的职业兴趣分为六种类型。根据真实感受作答，系统将为你生成个性化专业推荐报告。
            </p>
            <div class="progress-wrap">
                <div class="progress-bar">
                    <div class="progress-fill" id="progress-fill" style="width:0%"></div>
                </div>
                <p style="text-align:center;color:var(--text-secondary);font-weight:600;" id="progress-text">0 / 60 题已完成</p>
            </div>
        </div>
        <div id="questions-container"></div>
        <div class="card" style="text-align:center;padding:36px;">
            <button class="btn btn-primary btn-lg" onclick="submitTest()" id="submit-btn" disabled>提交测试 · 查看结果</button>
            <p style="margin-top:14px;color:var(--text-secondary);font-size:0.88rem;font-weight:500;" id="submit-hint">
                请完成全部60道题目后再提交
            </p>
        </div>
    </div>

    <!-- ========== 结果页面 ========== -->
    <div class="page" id="page-result">
        <div class="card" id="result-content">
            <h2>你的霍兰德测试结果</h2>
            <p style="color:var(--text-secondary);margin-bottom:16px;">请先完成测试以查看结果。</p>
        </div>
        <div id="result-detail" style="display:none;">
            <div class="card" id="scores-card"></div>
            <div class="card" id="recommend-card"></div>
            <div class="card" style="text-align:center;">
                <button class="btn btn-primary btn-lg" onclick="openReport()">查看完整报告</button>
                <button class="btn btn-outline btn-lg" style="margin-left:12px;" onclick="downloadReport()">下载报告 (PDF)</button>
            </div>
        </div>
    </div>

    <!-- ========== 热门专业介绍页面 ========== -->
    <div class="page" id="page-hotMajors">
        <div class="card">
            <h2>热门专业介绍</h2>
            <p style="color:var(--text-secondary);margin-bottom:20px;">
                结合近三年高考录取趋势和就业市场需求，以下专业持续火爆，发展前景广阔。
            </p>
            <div class="tabs" id="hot-tabs">
                <button class="tab active" onclick="switchHotTab('recent', this)">近三年热门</button>
                <button class="tab" onclick="switchHotTab('future', this)">未来潜力</button>
                <button class="tab" onclick="switchHotTab('analysis', this)">趋势分析</button>
            </div>
            <div id="hot-content"></div>
        </div>
    </div>

    <!-- ========== 专业查询页面 ========== -->
    <div class="page" id="page-majors">
        <div class="card">
            <h2>高考专业详细介绍</h2>
            <p style="color:var(--text-secondary);margin-bottom:16px;">
                涵盖12大学科门类，搜索或浏览了解各专业的培养目标、主要课程、就业方向等信息。
            </p>
            <div class="search-box">
                <input type="text" id="major-search" placeholder="搜索专业名称，如：计算机科学与技术、临床医学..." oninput="filterMajors()">
            </div>
            <div class="tabs" id="category-tabs"></div>
            <div class="major-list" id="major-list"></div>
        </div>
    </div>

    <!-- ========== 下载页面 ========== -->
    <div class="page" id="page-download">
        <div class="card">
            <h2>志翼翱翔高考志愿辅助系统</h2>
            <p style="color:var(--text-secondary);margin-bottom:20px;">
                下载志愿填报辅助系统，科学规划你的高考志愿。以下版本均为基础试用版，如需正式版请通过闲鱼小店购买。
            </p>
            <div class="download-grid" id="download-grid"></div>
        </div>
        <div class="card xianyu-section">
            <h2 style="justify-content:center;border-bottom:none;">获取正式版 & 全国各地高考数据</h2>
            <p class="qr-hint">使用闲鱼APP扫描下方二维码进入我的闲鱼小店</p>
            <img src="ewm.jpg" alt="闲鱼小店二维码" style="width:320px;max-width:95%;display:block;margin:0 auto;">
            <p style="color:var(--text-secondary);margin-top:14px;font-size:0.9rem;">
                提供：正式版志愿填报系统 | 各省历年录取数据 | 一分一段表 | 专业录取分数据
            </p>
        </div>
    </div>

</div>

<!-- Report Modal -->
<div class="modal-overlay" id="report-modal">
    <div class="modal" id="report-content">
        <button class="modal-close" onclick="closeReport()">&times;</button>
        <div id="report-body"></div>
    </div>
</div>

<!-- Footer -->
<div class="footer">
    &copy; 2025 志翼翱翔 | 霍兰德职业兴趣测试 | 数据仅供参考，具体请以官方发布为准
</div>

<script>
// ==================== DATA ====================

// 霍兰德测试题目（60题，每个类型10题）
var questions = [
    // R - 现实型（1-10）
    {id:1,type:'R',text:'我喜欢操作机器、使用工具来修理或制作物品。'},
    {id:2,type:'R',text:'我喜欢户外工作，比如种植、养殖或建造东西。'},
    {id:3,type:'R',text:'我喜欢动手组装模型、家具或电子设备。'},
    {id:4,type:'R',text:'我对机械原理和电子电路很感兴趣。'},
    {id:5,type:'R',text:'我喜欢运动，擅长需要身体协调的活动。'},
    {id:6,type:'R',text:'我更喜欢具体、实际的任务，而不是抽象的理论。'},
    {id:7,type:'R',text:'我喜欢驾驶车辆或操作大型机械。'},
    {id:8,type:'R',text:'我擅长使用各种工具进行手工制作。'},
    {id:9,type:'R',text:'我对建筑工程和施工技术感兴趣。'},
    {id:10,type:'R',text:'我喜欢将损坏的物品修复好。'},
    // I - 研究型（11-20）
    {id:11,type:'I',text:'我喜欢探索科学问题，寻找事物背后的原理。'},
    {id:12,type:'I',text:'我喜欢阅读科学类书籍和文章。'},
    {id:13,type:'I',text:'我喜欢做实验来验证假设。'},
    {id:14,type:'I',text:'我对数学推理和逻辑分析很感兴趣。'},
    {id:15,type:'I',text:'我喜欢独立思考和解决复杂问题。'},
    {id:16,type:'I',text:'我对自然现象和科学发现充满好奇。'},
    {id:17,type:'I',text:'我喜欢用数据和事实来分析问题。'},
    {id:18,type:'I',text:'我对编程、算法或人工智能感兴趣。'},
    {id:19,type:'I',text:'我喜欢进行深入的研究和调查。'},
    {id:20,type:'I',text:'我对医学研究和生物科技感兴趣。'},
    // A - 艺术型（21-30）
    {id:21,type:'A',text:'我喜欢绘画、雕塑、摄影等视觉艺术创作。'},
    {id:22,type:'A',text:'我喜欢音乐，会演奏乐器或喜欢唱歌。'},
    {id:23,type:'A',text:'我喜欢写作、诗歌或创意表达。'},
    {id:24,type:'A',text:'我对设计和美学有独特的见解。'},
    {id:25,type:'A',text:'我喜欢用创新的方式表达自己的想法。'},
    {id:26,type:'A',text:'我喜欢参观美术馆、博物馆或艺术展览。'},
    {id:27,type:'A',text:'我对戏剧、影视表演或导演感兴趣。'},
    {id:28,type:'A',text:'我喜欢创造独特的、个性化的作品。'},
    {id:29,type:'A',text:'我对时尚、室内设计或建筑设计感兴趣。'},
    {id:30,type:'A',text:'我喜欢用想象力创造新的事物。'},
    // S - 社会型（31-40）
    {id:31,type:'S',text:'我喜欢帮助他人解决困难。'},
    {id:32,type:'S',text:'我喜欢教学或培训他人。'},
    {id:33,type:'S',text:'我善于倾听他人的烦恼并提供支持。'},
    {id:34,type:'S',text:'我喜欢参加志愿活动或社区服务。'},
    {id:35,type:'S',text:'我善于与人沟通和建立关系。'},
    {id:36,type:'S',text:'我对心理学和人类行为很感兴趣。'},
    {id:37,type:'S',text:'我喜欢在团队中合作完成工作。'},
    {id:38,type:'S',text:'我对医疗护理或社会服务感兴趣。'},
    {id:39,type:'S',text:'我喜欢组织集体活动，促进团队和谐。'},
    {id:40,type:'S',text:'我善于理解他人的情绪和需求。'},
    // E - 企业型（41-50）
    {id:41,type:'E',text:'我喜欢领导和组织团队活动。'},
    {id:42,type:'E',text:'我对商业运营和创业很感兴趣。'},
    {id:43,type:'E',text:'我喜欢说服他人接受我的观点。'},
    {id:44,type:'E',text:'我善于制定目标和计划来达成目的。'},
    {id:45,type:'E',text:'我对市场营销和销售感兴趣。'},
    {id:46,type:'E',text:'我喜欢在竞争中获得成就感。'},
    {id:47,type:'E',text:'我善于做决策并承担风险。'},
    {id:48,type:'E',text:'我对政治、法律或管理感兴趣。'},
    {id:49,type:'E',text:'我喜欢在公众面前演讲或展示。'},
    {id:50,type:'E',text:'我善于发现商机并付诸行动。'},
    // C - 常规型（51-60）
    {id:51,type:'C',text:'我喜欢按照既定的流程和规范工作。'},
    {id:52,type:'C',text:'我善于整理文件和保持工作环境有序。'},
    {id:53,type:'C',text:'我对财务、会计或审计工作感兴趣。'},
    {id:54,type:'C',text:'我喜欢处理数据和制作报表。'},
    {id:55,type:'C',text:'我注重细节，能够发现细微的错误。'},
    {id:56,type:'C',text:'我喜欢在稳定、有规律的环境中工作。'},
    {id:57,type:'C',text:'我善于按照指示准确完成任务。'},
    {id:58,type:'C',text:'我对行政管理和办公事务感兴趣。'},
    {id:59,type:'C',text:'我喜欢制定和执行规章制度。'},
    {id:60,type:'C',text:'我善于管理时间和安排日程。'}
];

var typeInfo = {
    'R': {name:'现实型 (Realistic)',icon:'R',color:'#e67e22',desc:'动手能力强，喜欢具体、实际的任务。偏好户外或机械操作类工作。',traits:'务实、坦率、稳定、节俭、动手能力强'},
    'I': {name:'研究型 (Investigative)',icon:'I',color:'#3498db',desc:'善于观察、分析、推理，喜欢解决抽象问题。偏好科学研究类工作。',traits:'好奇、独立、理性、精确、善于分析'},
    'A': {name:'艺术型 (Artistic)',icon:'A',color:'#e74c3c',desc:'富有想象力和创造力，喜欢自由表达。偏好艺术、文学、设计类工作。',traits:'创新、感性、理想化、自由、善于表达'},
    'S': {name:'社会型 (Social)',icon:'S',color:'#2ecc71',desc:'乐于助人，善于沟通合作。偏好教育、医疗、社会服务类工作。',traits:'友善、热心、合作、理解、善于沟通'},
    'E': {name:'企业型 (Enterprising)',icon:'E',color:'#f39c12',desc:'有领导力，善于说服和影响他人。偏好管理、销售、政治类工作。',traits:'自信、雄心、果断、冒险、善于领导'},
    'C': {name:'常规型 (Conventional)',icon:'C',color:'#9b59b6',desc:'有条理、细致、可靠。偏好数据管理、行政、财务类工作。',traits:'谨慎、高效、有序、服从、自控力强'}
};

var majorsDB = [
    // 哲学
    {name:'哲学',category:'哲学',code:'010101',degree:'哲学学士',desc:'培养具有哲学理论思维能力和广博知识的专门人才。',courses:'哲学导论、中国哲学史、西方哲学史、逻辑学、伦理学、美学、宗教学、马克思主义哲学。',careers:'高校教师、研究员、公务员、编辑、文化传媒、企业管理咨询。',types:'I,A,S'},
    {name:'逻辑学',category:'哲学',code:'010102',degree:'哲学学士',desc:'研究思维规律和推理方法的学科。',courses:'数理逻辑、哲学逻辑、逻辑哲学、模态逻辑、集合论、证明论。',careers:'科研机构、高校、计算机科学相关、法律分析。',types:'I,C'},
    // 经济学
    {name:'经济学',category:'经济学',code:'020101',degree:'经济学学士',desc:'研究资源配置、经济运行规律的学科。',courses:'微观经济学、宏观经济学、计量经济学、政治经济学、经济史、金融学、国际贸易。',careers:'银行、证券公司、政府经济部门、研究机构、企业经济分析。',types:'I,E,C'},
    {name:'金融学',category:'经济学',code:'020301K',degree:'经济学学士',desc:'研究资金融通和金融市场运行的学科。',courses:'货币银行学、投资学、公司金融、国际金融、金融市场学、风险管理。',careers:'银行、证券、保险、基金、信托、金融监管机构。',types:'E,C,I'},
    {name:'国际经济与贸易',category:'经济学',code:'020401',degree:'经济学学士',desc:'研究国际贸易理论和实务操作的学科。',courses:'国际贸易理论、国际金融、国际贸易实务、国际结算、外贸英语、国际商法。',careers:'外贸公司、跨国公司、海关、商务部门、国际物流。',types:'E,S,C'},
    // 法学
    {name:'法学',category:'法学',code:'030101K',degree:'法学学士',desc:'系统学习法律理论和实务的学科。',courses:'法理学、宪法学、民法、刑法、行政法、经济法、国际法、诉讼法。',careers:'律师、法官、检察官、公务员、企业法务、公证员。',types:'E,I,S'},
    {name:'社会学',category:'法学',code:'030301',degree:'法学学士',desc:'研究社会结构、社会关系和社会变迁的学科。',courses:'社会学概论、社会研究方法、社会心理学、社会统计学、城市社会学。',careers:'政府机构、社会组织、市场调研、社区管理、人力资源管理。',types:'I,S,A'},
    // 教育学
    {name:'教育学',category:'教育学',code:'040101',degree:'教育学学士',desc:'研究教育现象、教育规律和教育管理的学科。',courses:'教育学原理、教育心理学、中外教育史、课程与教学论、教育研究方法。',careers:'教师、教育行政、教育培训、教育研究、教育出版社。',types:'S,I,C'},
    {name:'学前教育',category:'教育学',code:'040106',degree:'教育学学士',desc:'培养具备学前教育专业知识和技能的专门人才。',courses:'学前儿童发展心理学、学前教育学、学前卫生学、幼儿园课程、儿童游戏理论。',careers:'幼儿园教师、早教机构、儿童教育产品开发、学前教育管理。',types:'S,A,C'},
    // 文学
    {name:'汉语言文学',category:'文学',code:'050101',degree:'文学学士',desc:'研究中国语言和文学的专业。',courses:'古代汉语、现代汉语、中国古代文学、中国现当代文学、外国文学、文学理论、语言学概论。',careers:'教师、编辑、记者、文案策划、公务员、文化传媒。',types:'A,S,I'},
    {name:'新闻学',category:'文学',code:'050301',degree:'文学学士',desc:'研究新闻传播规律和新闻实务的学科。',courses:'新闻学概论、传播学、新闻采访与写作、新闻编辑、新闻摄影、新媒体概论。',careers:'记者、编辑、新媒体运营、公关、广告策划、广播电视。',types:'A,S,E'},
    // 理学
    {name:'数学与应用数学',category:'理学',code:'070101',degree:'理学学士',desc:'研究数学理论和应用的学科。',courses:'数学分析、高等代数、概率论与数理统计、常微分方程、数值分析、数学建模。',careers:'教师、金融量化分析、数据分析师、软件开发、科研。',types:'I,C,R'},
    {name:'物理学',category:'理学',code:'070201',degree:'理学学士',desc:'研究物质运动最一般规律和物质基本结构的学科。',courses:'力学、热学、电磁学、光学、量子力学、固体物理、理论力学。',careers:'科研机构、高校教师、半导体行业、光学工程、核能。',types:'I,R,C'},
    {name:'化学',category:'理学',code:'070301',degree:'理学学士',desc:'研究物质组成、结构、性质和变化规律的学科。',courses:'无机化学、有机化学、分析化学、物理化学、高分子化学、生物化学。',careers:'化工企业、制药公司、检测机构、科研院所、教师。',types:'I,R,C'},
    {name:'生物科学',category:'理学',code:'071001',degree:'理学学士',desc:'研究生命现象和生物活动规律的学科。',courses:'植物学、动物学、微生物学、生物化学、遗传学、细胞生物学、分子生物学。',careers:'生物医药、科研机构、教师、环保部门、食品行业。',types:'I,R,A'},
    {name:'心理学',category:'理学',code:'071101',degree:'理学学士',desc:'研究人类心理现象和行为规律的学科。',courses:'普通心理学、实验心理学、发展心理学、社会心理学、认知心理学、心理统计。',careers:'心理咨询师、人力资源、教育咨询、市场研究、临床心理。',types:'I,S,A'},
    // 工学
    {name:'计算机科学与技术',category:'工学',code:'080901',degree:'工学学士',desc:'研究计算机系统、算法和软件开发的学科。',courses:'数据结构、操作系统、计算机网络、数据库原理、算法设计、编译原理、软件工程。',careers:'软件工程师、算法工程师、系统架构师、网络安全、产品经理。',types:'I,R,C'},
    {name:'软件工程',category:'工学',code:'080902',degree:'工学学士',desc:'系统学习软件开发和项目管理的学科。',courses:'软件工程概论、需求工程、软件测试、软件项目管理、人机交互、面向对象程序设计。',careers:'软件开发、测试工程师、项目经理、技术总监、DevOps工程师。',types:'I,R,C'},
    {name:'人工智能',category:'工学',code:'080717T',degree:'工学学士',desc:'研究智能系统和机器学习的前沿学科。',courses:'机器学习、深度学习、自然语言处理、计算机视觉、数据挖掘、强化学习。',careers:'AI工程师、算法研究员、数据科学家、智能产品开发、自动驾驶。',types:'I,R,C'},
    {name:'电子信息工程',category:'工学',code:'080701',degree:'工学学士',desc:'研究电子技术和信息系统的学科。',courses:'电路分析、模拟电子技术、数字电子技术、信号与系统、通信原理、嵌入式系统。',careers:'电子工程师、通信工程师、嵌入式开发、芯片设计、物联网。',types:'R,I,C'},
    {name:'电气工程及其自动化',category:'工学',code:'080601',degree:'工学学士',desc:'研究电能的产生、传输和应用技术的学科。',courses:'电路、电机学、电力系统分析、电力电子技术、自动控制原理、PLC原理及应用。',careers:'电力公司、电气设备制造、自动化工程师、新能源、轨道交通。',types:'R,I,C'},
    {name:'机械工程',category:'工学',code:'080201',degree:'工学学士',desc:'研究机械设计、制造和自动化技术的学科。',courses:'机械制图、理论力学、材料力学、机械设计、机械制造工艺、液压与气动。',careers:'机械设计工程师、制造工程师、汽车行业、航空航天、机器人。',types:'R,I,C'},
    {name:'土木工程',category:'工学',code:'081001',degree:'工学学士',desc:'研究建筑、道路、桥梁等基础设施的设计和施工。',courses:'结构力学、土力学、混凝土结构、钢结构、土木工程施工、工程测量学。',careers:'结构工程师、施工管理、监理工程师、房地产开发、市政工程。',types:'R,I,C'},
    {name:'建筑学',category:'工学',code:'082801',degree:'建筑学学士',desc:'研究建筑设计和空间规划的综合学科。',courses:'建筑设计、建筑历史、建筑构造、建筑物理、城市规划、景观设计。',careers:'建筑师、城市规划师、室内设计师、房地产策划、古建保护。',types:'A,R,I'},
    {name:'数据科学与大数据技术',category:'工学',code:'080910T',degree:'工学学士',desc:'研究大规模数据处理、分析和应用的前沿学科。',courses:'大数据技术、数据挖掘、机器学习、分布式计算、数据可视化、统计学。',careers:'数据分析师、大数据工程师、数据科学家、商业智能、金融科技。',types:'I,C,R'},
    // 农学
    {name:'农学',category:'农学',code:'090101',degree:'农学学士',desc:'研究农作物生产与农业技术的学科。',courses:'植物生理学、遗传学、作物栽培学、土壤肥料学、植物保护、种子学。',careers:'农业技术推广、种子公司、农业科研、农业管理、生态农业。',types:'R,I,C'},
    // 医学
    {name:'临床医学',category:'医学',code:'100201K',degree:'医学学士',desc:'培养具备基础医学和临床医学知识与技能的医师。',courses:'人体解剖学、生理学、病理学、药理学、诊断学、内科学、外科学、妇产科学。',careers:'医生、医学研究、医药企业、公共卫生、医学教育。',types:'I,S,R'},
    {name:'口腔医学',category:'医学',code:'100301K',degree:'医学学士',desc:'培养口腔疾病诊疗和预防的专业医师。',courses:'口腔解剖生理学、口腔组织病理学、牙体牙髓病学、口腔修复学、口腔颌面外科学。',careers:'口腔医生、口腔医疗器械研发、口腔医学教育。',types:'I,R,S'},
    {name:'药学',category:'医学',code:'100701',degree:'理学学士',desc:'研究药物制备、质量控制和应用的科学。',courses:'药物化学、药剂学、药理学、药物分析、天然药物化学、药事管理。',careers:'药剂师、药品研发、药品生产管理、药品检验、医药代表。',types:'I,C,R'},
    {name:'护理学',category:'医学',code:'101101',degree:'理学学士',desc:'培养具备临床护理和护理管理能力的专业人才。',courses:'护理学基础、内科护理学、外科护理学、妇产科护理学、儿科护理学、护理管理。',careers:'护士、护理管理、社区护理、护理教育、养老产业。',types:'S,R,C'},
    // 管理学
    {name:'工商管理',category:'管理学',code:'120201K',degree:'管理学学士',desc:'系统学习企业管理理论和实践的学科。',courses:'管理学原理、组织行为学、人力资源管理、市场营销、财务管理、战略管理。',careers:'企业管理、咨询顾问、人力资源管理、市场营销、创业。',types:'E,S,C'},
    {name:'会计学',category:'管理学',code:'120203K',degree:'管理学学士',desc:'研究财务核算、审计和财务管理的学科。',courses:'基础会计、中级财务会计、成本会计、管理会计、审计学、税法、财务管理。',careers:'注册会计师、审计师、财务经理、税务顾问、财务分析。',types:'C,I,E'},
    {name:'电子商务',category:'管理学',code:'120801',degree:'管理学学士',desc:'研究互联网商务模式和运营的学科。',courses:'电子商务概论、网络营销、供应链管理、电子支付、电子商务法律、数据分析。',careers:'电商运营、互联网产品经理、数字营销、跨境电商、直播运营。',types:'E,C,R'},
    // 艺术学
    {name:'视觉传达设计',category:'艺术学',code:'130502',degree:'艺术学学士',desc:'研究视觉信息设计和传播的学科。',courses:'设计基础、字体设计、版式设计、品牌设计、交互设计、包装设计。',careers:'平面设计师、UI/UX设计师、品牌策划、广告设计、插画师。',types:'A,R,C'},
    {name:'数字媒体艺术',category:'艺术学',code:'130508',degree:'艺术学学士',desc:'研究数字技术与艺术融合的学科。',courses:'数字影像、交互设计、三维建模、动画原理、游戏设计、影视特效。',careers:'游戏设计、影视后期、动画制作、新媒体艺术、VR/AR开发。',types:'A,R,I'}
];

var downloadFiles = [
    {name:'志翼翱翔高考志愿辅助系统（机构试用版）',url:'https://www.guangyapan.com/s/1907275797558620185_aeytXClUAO4ed4BG',desc:'适合学校、培训机构等团体使用。',iconClass:'school',iconText:'机构'},
    {name:'志翼翱翔高考志愿辅助系统（考生试用版）',url:'https://www.guangyapan.com/s/1907276018703343677_aeytXClUAO4ed4BG',desc:'适合考生个人使用，智能推荐志愿方案。',iconClass:'student',iconText:'考生'},
    {name:'志翼翱翔山东省春考志愿辅助系统（机构试用版）',url:'https://www.guangyapan.com/s/1907276195958825000_aeytXClUAO4ed4BG',desc:'山东省春季高考专用，机构版本。',iconClass:'shandong',iconText:'鲁春'},
    {name:'志翼翱翔山东省春考志愿辅助系统（考生试用版）',url:'https://www.guangyapan.com/s/1907276352741863519_aeytXClUAO4ed4BG',desc:'山东省春季高考专用，考生版本。',iconClass:'shandong',iconText:'鲁春'}
];

// 热门专业数据
var hotMajorsRecent = [
    {
        name:'人工智能',
        category:'工学',
        icon:'AI',
        color:'#6366f1',
        rank:'第1名',
        reason:'AI技术全面渗透各行各业，ChatGPT等大模型引爆全球AI革命，人才缺口超500万。连续三年蝉联最热专业榜首，顶尖院校录取分数屡创新高。',
        salary:'应届生平均起薪25-50万/年',
        trend:'持续火爆，未来5年需求只增不减',
        schools:'清华大学、北京大学、浙江大学、上海交通大学、南京大学、中国科学技术大学、哈尔滨工业大学',
        tips:'建议数学和编程基础扎实的同学报考，竞争非常激烈，需提前规划。'
    },
    {
        name:'数据科学与大数据技术',
        category:'工学',
        icon:'DS',
        color:'#3b82f6',
        rank:'第2名',
        reason:'数字化转型加速，数据成为核心生产要素。企业急需数据人才驱动决策，金融、电商、医疗等行业需求旺盛。',
        salary:'应届生平均起薪18-35万/年',
        trend:'持续增长，企业数字化推动需求扩大',
        schools:'北京大学、清华大学、中国人民大学、复旦大学、武汉大学、华中科技大学、北京邮电大学',
        tips:'数学统计能力强是优势，编程能力可逐步培养，就业面极广。'
    },
    {
        name:'计算机科学与技术',
        category:'工学',
        icon:'CS',
        color:'#1e40af',
        rank:'第3名',
        reason:'互联网和科技行业的核心基础专业，就业面最广的工科专业。软件开发、网络安全、系统架构等方向人才需求稳定且巨大。',
        salary:'应届生平均起薪15-30万/年',
        trend:'需求稳定增长，是"万金油"专业',
        schools:'清华大学、北京大学、浙江大学、国防科技大学、北京航空航天大学、华中科技大学、电子科技大学',
        tips:'编程零基础也可报考，大学期间多做项目积累经验，就业选择非常灵活。'
    },
    {
        name:'临床医学',
        category:'医学',
        icon:'医',
        color:'#ef4444',
        rank:'第4名',
        reason:'人口老龄化和健康意识提升推动医疗需求爆发式增长。医生职业稳定性强、社会地位高，疫情后医学专业热度大幅攀升。',
        salary:'三甲医院住院医约10-15万/年，资深医生30-80万/年',
        trend:'持续增长，医疗健康是永远的朝阳产业',
        schools:'北京协和医学院、北京大学、复旦大学、上海交通大学、中山大学、四川大学、华中科技大学',
        tips:'学习周期长（5年本科+3年规培），需要强大毅力和责任心，但回报同样丰厚。'
    },
    {
        name:'软件工程',
        category:'工学',
        icon:'SE',
        color:'#0d9488',
        rank:'第5名',
        reason:'移动互联网、云计算、企业数字化转型持续推动软件人才需求。相比计科更侧重工程实践，就业导向强。',
        salary:'应届生平均起薪15-28万/年',
        trend:'需求旺盛，DevOps和云原生方向火热',
        schools:'北京大学、清华大学、北京航空航天大学、浙江大学、华东师范大学、南京大学、武汉大学',
        tips:'实践能力比理论更重要，建议多参与开源项目和实习，大厂校招机会多。'
    },
    {
        name:'电子信息工程',
        category:'工学',
        icon:'EE',
        color:'#f59e0b',
        rank:'第6名',
        reason:'5G通信、芯片产业和物联网的高速发展，使得电子信息人才极度紧缺。国家芯片战略推动下，集成电路方向薪资暴涨。',
        salary:'应届生平均起薪15-30万/年，芯片方向可达25-40万',
        trend:'芯片国产化浪潮下爆发式增长',
        schools:'电子科技大学、西安电子科技大学、清华大学、北京大学、东南大学、北京邮电大学、上海交通大学',
        tips:'物理和数学基础要好，芯片/半导体方向前景极佳，是国家战略支持领域。'
    },
    {
        name:'金融学',
        category:'经济学',
        icon:'金',
        color:'#d97706',
        rank:'第7名',
        reason:'金融科技（FinTech）兴起，传统金融与科技融合创造大量高薪岗位。量化交易、风险管理等方向人才供不应求。',
        salary:'应届生平均起薪12-25万/年，投行/量化可达30-60万',
        trend:'需求稳定，金融科技是增长亮点',
        schools:'北京大学、清华大学、中国人民大学、复旦大学、上海财经大学、中央财经大学、对外经济贸易大学',
        tips:'数学好+懂编程的复合型金融人才最吃香，建议辅修计算机或统计学。'
    },
    {
        name:'电气工程及其自动化',
        category:'工学',
        icon:'电',
        color:'#e67e22',
        rank:'第8名',
        reason:'新能源汽车、智能电网、光伏风电等新能源产业爆发，电气工程人才需求激增。国家电网等央企招聘量巨大。',
        salary:'应届生起薪10-20万/年，新能源车企15-25万',
        trend:'新能源浪潮推动需求爆发',
        schools:'清华大学、西安交通大学、华中科技大学、浙江大学、华北电力大学、哈尔滨工业大学、重庆大学',
        tips:'进国家电网是稳定高福利的经典选择，新能源方向更有爆发力，就业不愁。'
    }
];

var hotMajorsFuture = [
    {
        name:'集成电路设计与集成系统',
        category:'工学',
        icon:'IC',
        color:'#8b5cf6',
        reason:'芯片"卡脖子"问题使国家全力投入半导体产业，未来10年将持续受到政策和资本双重驱动。国产替代带来海量岗位。',
        salary:'预计起薪25-40万/年',
        growth:'未来5年需求增速超30%',
        schools:'电子科技大学、西安电子科技大学、清华大学、北京大学、中国科学院大学、复旦大学',
        keywords:'国产芯片、半导体、EDA工具、先进制程'
    },
    {
        name:'生物医学工程',
        category:'工学',
        icon:'医工',
        color:'#10b981',
        reason:'老龄化社会对医疗器械、康复设备需求激增，脑机接口、基因编辑等前沿技术突破带来新机遇。',
        salary:'预计起薪15-25万/年',
        growth:'未来5年需求增速超25%',
        schools:'清华大学、上海交通大学、浙江大学、华中科技大学、东南大学、天津大学',
        keywords:'医疗器械、脑机接口、康复工程、智能穿戴'
    },
    {
        name:'新能源科学与工程',
        category:'工学',
        icon:'新能源',
        color:'#f59e0b',
        reason:'碳中和目标下，光伏、风电、储能、氢能等新能源领域将成为未来30年的核心产业。政策扶持力度空前。',
        salary:'预计起薪15-25万/年',
        growth:'未来5年需求增速超40%',
        schools:'西安交通大学、华中科技大学、华北电力大学、上海交通大学、天津大学、重庆大学',
        keywords:'碳中和、光伏、储能、氢能、智能电网'
    },
    {
        name:'网络安全',
        category:'工学',
        icon:'安',
        color:'#ef4444',
        reason:'数字化时代网络攻击日益频繁，国家网络安全战略上升至前所未有的高度。数据安全法实施催生大量合规岗位。',
        salary:'预计起薪18-35万/年',
        growth:'未来5年需求增速超35%',
        schools:'国防科技大学、北京邮电大学、西安电子科技大学、电子科技大学、上海交通大学、武汉大学',
        keywords:'信息安全、渗透测试、数据安全、密码学'
    },
    {
        name:'心理学',
        category:'理学',
        icon:'心理',
        color:'#ec4899',
        reason:'社会压力增大，心理健康需求爆发式增长。青少年心理咨询、企业EAP服务、用户体验研究等新兴方向前景广阔。',
        salary:'预计起薪8-18万/年，资深咨询师30万+',
        growth:'未来5年需求增速超30%',
        schools:'北京师范大学、北京大学、华东师范大学、华南师范大学、浙江大学、西南大学',
        keywords:'心理咨询、用户研究、组织心理学、教育心理'
    },
    {
        name:'数字媒体技术/艺术',
        category:'艺术学',
        icon:'数字',
        color:'#f43f5e',
        reason:'元宇宙、游戏产业、短视频、虚拟现实等数字内容产业持续爆发。AI绘画/视频工具的出现不是威胁而是新机遇。',
        salary:'预计起薪12-25万/年',
        growth:'未来5年需求增速超25%',
        schools:'中国传媒大学、北京电影学院、中央美术学院、浙江大学、上海大学、南京艺术学院',
        keywords:'游戏开发、元宇宙、VR/AR、AI艺术、短视频'
    },
    {
        name:'健康服务与管理',
        category:'管理学',
        icon:'健康',
        color:'#14b8a6',
        reason:'老龄化社会催生银发经济，健康管理、养老产业成为万亿级市场。社区医疗、康养旅游等新模式不断涌现。',
        salary:'预计起薪10-18万/年',
        growth:'未来5年需求增速超30%',
        schools:'中国人民大学、复旦大学、华中科技大学、中山大学、四川大学、南方医科大学',
        keywords:'养老产业、健康管理、银发经济、康养旅游'
    },
    {
        name:'机器人工程',
        category:'工学',
        icon:'机器人',
        color:'#6366f1',
        reason:'工业机器人和服务机器人市场高速增长，智能制造是制造业升级的核心。人形机器人突破带来全新想象空间。',
        salary:'预计起薪18-30万/年',
        growth:'未来5年需求增速超35%',
        schools:'哈尔滨工业大学、北京航空航天大学、上海交通大学、浙江大学、华中科技大学、清华大学',
        keywords:'智能制造、人形机器人、自动驾驶、工业4.0'
    }
];

// ==================== STATE ====================
var answers = {};
var currentScores = null;

// ==================== NAVIGATION ====================
function showPage(page, btn) {
    document.querySelectorAll('.page').forEach(function(p) { p.classList.remove('active'); });
    document.querySelectorAll('.nav-btn').forEach(function(b) { b.classList.remove('active'); });
    document.getElementById('page-' + page).classList.add('active');
    if (btn) btn.classList.add('active');
    if (page === 'result' && currentScores) renderResults();
}

// ==================== QUESTIONS ====================
function renderQuestions() {
    var container = document.getElementById('questions-container');
    container.innerHTML = '';
    questions.forEach(function(q, idx) {
        var div = document.createElement('div');
        div.className = 'question-block';
        div.innerHTML =
            '<div class="question-text">' + (idx + 1) + '. ' + q.text + '</div>' +
            '<div class="options">' +
                '<button class="option-btn" onclick="selectAnswer(' + q.id + ', 5, this)">非常符合</button>' +
                '<button class="option-btn" onclick="selectAnswer(' + q.id + ', 4, this)">比较符合</button>' +
                '<button class="option-btn" onclick="selectAnswer(' + q.id + ', 3, this)">一般</button>' +
                '<button class="option-btn" onclick="selectAnswer(' + q.id + ', 2, this)">不太符合</button>' +
                '<button class="option-btn" onclick="selectAnswer(' + q.id + ', 1, this)">很不符合</button>' +
            '</div>';
        container.appendChild(div);
    });
}

function selectAnswer(qid, score, btn) {
    answers[qid] = score;
    var parent = btn.parentElement;
    parent.querySelectorAll('.option-btn').forEach(function(b) { b.classList.remove('selected'); });
    btn.classList.add('selected');
    updateProgress();
}

function updateProgress() {
    var answered = Object.keys(answers).length;
    var total = questions.length;
    var pct = Math.round((answered / total) * 100);
    document.getElementById('progress-fill').style.width = pct + '%';
    document.getElementById('progress-text').textContent = answered + ' / ' + total + ' 题已完成';
    var submitBtn = document.getElementById('submit-btn');
    var hint = document.getElementById('submit-hint');
    if (answered === total) {
        submitBtn.disabled = false;
        hint.textContent = '所有题目已完成，点击提交查看结果！';
        hint.style.color = '#0d9488';
    } else {
        submitBtn.disabled = true;
        hint.textContent = '请完成全部' + total + '道题目后再提交（还剩' + (total - answered) + '题）';
        hint.style.color = '#64748b';
    }
}

function submitTest() {
    if (Object.keys(answers).length < questions.length) {
        alert('请完成全部题目后再提交！');
        return;
    }
    var scores = {R:0,I:0,A:0,S:0,E:0,C:0};
    questions.forEach(function(q) {
        scores[q.type] += (answers[q.id] || 3);
    });
    currentScores = scores;
    renderResults();
    showPage('result', document.getElementById('nav-result'));
    document.getElementById('page-result').scrollIntoView({behavior:'smooth'});
}

// ==================== RESULTS ====================
function renderResults() {
    if (!currentScores) return;
    var scores = currentScores;
    var sorted = Object.entries(scores).sort(function(a,b) { return b[1] - a[1]; });
    var top3 = sorted.slice(0, 3);
    var hollandCode = top3.map(function(s) { return s[0]; }).join('');

    // Scores card
    var scoresCard = document.getElementById('scores-card');
    scoresCard.innerHTML = '<h2>六种类型得分</h2>';
    Object.keys(typeInfo).forEach(function(key) {
        var info = typeInfo[key];
        var pct = Math.round((scores[key] / 50) * 100);
        var isTop = top3.some(function(t) { return t[0] === key; });
        scoresCard.innerHTML +=
            '<div class="type-card' + (isTop ? ' high' : '') + '">' +
                '<strong><span style="display:inline-block;width:24px;height:24px;border-radius:50%;background:' + info.color + ';color:white;text-align:center;line-height:24px;font-size:0.75rem;margin-right:6px;">' + info.icon + '</span>' + info.name + '</strong>' +
                '<div class="type-bar">' +
                    '<div class="type-bar-fill" style="width:' + pct + '%;background:' + info.color + ';">' + scores[key] + '</div>' +
                '</div>' +
                '<small style="color:var(--text-secondary);">' + info.desc + '</small>' +
            '</div>';
    });

    // Recommend card
    var recommendedMajors = getRecommendedMajors(top3);
    var recommendCard = document.getElementById('recommend-card');
    var topTypeName = typeInfo[top3[0][0]].name;
    var secTypeName = typeInfo[top3[1][0]].name;
    var thirdTypeName = typeInfo[top3[2][0]].name;
    var codeBadges = '';
    top3.forEach(function(s) {
        var info = typeInfo[s[0]];
        codeBadges += '<span style="background:' + info.color + ';">' + info.icon + '</span>';
    });
    recommendCard.innerHTML =
        '<h2>你的霍兰德代码</h2>' +
        '<div class="holland-code-badge">' + codeBadges + '</div>' +
        '<p style="margin:8px 0 16px;font-size:1.3rem;font-weight:800;color:#4f46e5;letter-spacing:4px;">' + hollandCode + '</p>' +
        '<p style="margin-bottom:16px;color:var(--text-secondary);">' +
            '主导类型：<strong>' + topTypeName + '</strong>，结合<strong>' + secTypeName + '</strong>和<strong>' + thirdTypeName + '</strong>。以下专业可能非常适合你：' +
        '</p>' +
        '<div class="major-list">' +
            recommendedMajors.slice(0, 12).map(function(m) {
                return '<div class="major-item" onclick="showMajorDetail(\'' + m.name + '\')">' +
                    '<div class="major-name">' + m.name + '</div>' +
                    '<div class="major-match">匹配度：' + m.match + '% | ' + m.category + '</div>' +
                '</div>';
            }).join('') +
        '</div>';

    document.getElementById('result-detail').style.display = 'block';
}

function getRecommendedMajors(top3) {
    var topTypes = top3.map(function(t) { return t[0]; });
    var results = [];
    majorsDB.forEach(function(major) {
        var match = 0;
        var majorTypes = major.types.split(',');
        majorTypes.forEach(function(t, idx) {
            if (topTypes.indexOf(t) >= 0) {
                match += (3 - idx) * (topTypes.length - topTypes.indexOf(t));
            }
        });
        var maxPossible = 3 * 3 + 2 * 2 + 1 * 1;
        var matchPct = Math.min(100, Math.round((match / maxPossible) * 100));
        if (matchPct >= 40) {
            results.push({name: major.name, category: major.category, match: matchPct});
        }
    });
    return results.sort(function(a,b) { return b.match - a.match; });
}

// ==================== REPORT ====================
function openReport() {
    if (!currentScores) return;
    var scores = currentScores;
    var sorted = Object.entries(scores).sort(function(a,b) { return b[1] - a[1]; });
    var top3 = sorted.slice(0, 3);
    var hollandCode = top3.map(function(s) { return s[0]; }).join('');
    var recommendedMajors = getRecommendedMajors(top3);
    var now = new Date().toLocaleDateString('zh-CN', {year:'numeric',month:'long',day:'numeric'});

    var scoresHTML = '';
    Object.keys(typeInfo).forEach(function(key) {
        var info = typeInfo[key];
        var pct = Math.round((scores[key] / 50) * 100);
        var isTop = top3.some(function(t) { return t[0] === key; });
        scoresHTML +=
            '<div style="margin-bottom:10px;' + (isTop ? 'background:#f0fdf4;padding:10px;border-radius:8px;' : '') + '">' +
                '<strong><span style="display:inline-block;width:24px;height:24px;border-radius:50%;background:' + info.color + ';color:white;text-align:center;line-height:24px;font-size:0.75rem;margin-right:6px;">' + info.icon + '</span>' + info.name + '</strong>：' + scores[key] + ' 分 / 50' +
                '<div style="background:#e2e8f0;height:10px;border-radius:5px;margin-top:4px;">' +
                    '<div style="width:' + pct + '%;height:100%;background:' + info.color + ';border-radius:5px;"></div>' +
                '</div>' +
            '</div>';
    });

    var typeInterpretHTML = '';
    top3.forEach(function(arr, i) {
        var key = arr[0];
        var score = arr[1];
        var info = typeInfo[key];
        typeInterpretHTML +=
            '<div style="margin-bottom:16px;padding:12px;background:#f8fafc;border-radius:8px;border-left:4px solid ' + info.color + ';">' +
                '<strong style="font-size:1.1rem;">' + (i+1) + '. <span style="display:inline-block;width:24px;height:24px;border-radius:50%;background:' + info.color + ';color:white;text-align:center;line-height:24px;font-size:0.75rem;margin-right:4px;">' + info.icon + '</span> ' + info.name + '</strong>（' + score + '分）' +
                '<p style="margin:4px 0;color:#475569;">' + info.desc + '</p>' +
                '<p style="font-size:0.9rem;color:#64748b;">典型特质：' + info.traits + '</p>' +
            '</div>';
    });

    var majorsHTML = '';
    recommendedMajors.slice(0, 15).forEach(function(m) {
        majorsHTML +=
            '<div style="padding:10px;background:#f0f9ff;border-radius:8px;border:1px solid #bae6fd;">' +
                '<strong>' + m.name + '</strong><br>' +
                '<small style="color:#0d9488;">匹配度：' + m.match + '%</small><br>' +
                '<small style="color:#64748b;">' + m.category + '</small>' +
            '</div>';
    });

    var reportHTML =
        '<div style="text-align:center;margin-bottom:24px;">' +
            '<h1 style="color:#1e40af;font-size:1.6rem;">志翼翱翔</h1>' +
            '<h2 style="font-size:1.3rem;color:#334155;">霍兰德职业兴趣测试报告</h2>' +
            '<p style="color:#64748b;">测试日期：' + now + '</p>' +
        '</div>' +
        '<hr style="border:1px solid #e2e8f0;margin:20px 0;">' +
        '<h3 style="color:#1e40af;">你的霍兰德代码：<span style="font-size:1.4rem;">' + hollandCode + '</span></h3>' +
        '<p style="color:#64748b;margin-bottom:16px;">以下是你六种职业兴趣类型的得分情况：</p>' +
        scoresHTML +
        '<hr style="border:1px solid #e2e8f0;margin:20px 0;">' +
        '<h3 style="color:#1e40af;">类型解读</h3>' +
        typeInterpretHTML +
        '<hr style="border:1px solid #e2e8f0;margin:20px 0;">' +
        '<h3 style="color:#1e40af;">推荐专业方向</h3>' +
        '<div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:8px;">' +
            majorsHTML +
        '</div>' +
        '<hr style="border:1px solid #e2e8f0;margin:20px 0;">' +
        '<h3 style="color:#1e40af;">发展建议</h3>' +
        '<ul style="color:#475569;line-height:1.8;">' +
            '<li>你的主导类型：<strong>' + typeInfo[top3[0][0]].name + '</strong>，建议优先考虑与该类型匹配的专业方向。</li>' +
            '<li>选择专业时，综合考虑兴趣、能力和就业前景，找到三者的平衡点。</li>' +
            '<li>大学期间可以通过辅修、社团活动等方式发展多元能力。</li>' +
            '<li>建议使用"志翼翱翔高考志愿辅助系统"进行更精准的志愿填报规划。</li>' +
        '</ul>' +
        '<div style="text-align:center;margin-top:24px;padding:16px;background:#fefce8;border-radius:8px;">' +
            '<p style="color:#92400e;font-size:0.9rem;">如需正式版志愿填报系统及全国各地高考数据</p>' +
            '<p style="color:#ef4444;font-weight:600;">请用闲鱼APP扫描二维码进入我的小店</p>' +
        '</div>' +
        '<p style="text-align:center;color:#94a3b8;font-size:0.8rem;margin-top:20px;">' +
            '本报告由志翼翱翔自动生成 | 仅供参考，具体志愿填报请以官方信息为准' +
        '</p>';

    document.getElementById('report-body').innerHTML = reportHTML;
    document.getElementById('report-modal').classList.add('show');
}

function closeReport() {
    document.getElementById('report-modal').classList.remove('show');
}

function downloadReport() {
    if (!currentScores) return;
    openReport();
    setTimeout(function() {
        window.print();
    }, 500);
}

// ==================== MAJORS ====================
function renderCategoryTabs() {
    var cats = [];
    majorsDB.forEach(function(m) {
        if (cats.indexOf(m.category) === -1) cats.push(m.category);
    });
    var tabsContainer = document.getElementById('category-tabs');
    tabsContainer.innerHTML =
        '<button class="tab active" onclick="filterByCategory(\'all\', this)">全部</button>' +
        cats.map(function(c) {
            return '<button class="tab" onclick="filterByCategory(\'' + c + '\', this)">' + c + '</button>';
        }).join('');
}

function filterByCategory(category, btn) {
    document.querySelectorAll('#category-tabs .tab').forEach(function(t) { t.classList.remove('active'); });
    btn.classList.add('active');
    var filtered = category === 'all' ? majorsDB : majorsDB.filter(function(m) { return m.category === category; });
    renderMajorList(filtered);
}

function filterMajors() {
    var query = document.getElementById('major-search').value.toLowerCase();
    var filtered = majorsDB.filter(function(m) {
        return m.name.toLowerCase().indexOf(query) >= 0 ||
               m.category.toLowerCase().indexOf(query) >= 0 ||
               m.desc.toLowerCase().indexOf(query) >= 0;
    });
    renderMajorList(filtered);
    document.querySelectorAll('#category-tabs .tab').forEach(function(t) { t.classList.remove('active'); });
    var firstTab = document.querySelector('#category-tabs .tab');
    if (firstTab) firstTab.classList.add('active');
}

function renderMajorList(list) {
    var container = document.getElementById('major-list');
    container.innerHTML = list.map(function(m) {
        return '<div class="major-item" onclick="showMajorDetail(\'' + m.name + '\')">' +
            '<div class="major-name">' + m.name + '</div>' +
            '<div style="font-size:0.85rem;color:var(--text-secondary);">' + m.category + ' · ' + m.degree + '</div>' +
            '<div style="font-size:0.82rem;color:#64748b;margin-top:4px;">' + m.desc + '</div>' +
        '</div>';
    }).join('');
}

function showMajorDetail(name) {
    var major = null;
    for (var i = 0; i < majorsDB.length; i++) {
        if (majorsDB[i].name === name) { major = majorsDB[i]; break; }
    }
    if (!major) return;

    var typesStr = major.types.split(',').map(function(t) {
        return typeInfo[t] ? typeInfo[t].name : t;
    }).join('、');

    var modal = document.getElementById('report-body');
    modal.innerHTML =
        '<div style="text-align:center;margin-bottom:20px;">' +
            '<h2 style="color:#1e40af;">' + major.name + '</h2>' +
            '<span style="background:#eff6ff;color:#1e40af;padding:4px 12px;border-radius:12px;font-size:0.9rem;">' + major.category + '</span>' +
        '</div>' +
        '<div style="margin-bottom:16px;">' +
            '<strong>专业代码：</strong>' + major.code + '<br>' +
            '<strong>授予学位：</strong>' + major.degree +
        '</div>' +
        '<div style="margin-bottom:16px;">' +
            '<h4 style="color:#334155;">专业介绍</h4>' +
            '<p style="color:#475569;">' + major.desc + '</p>' +
        '</div>' +
        '<div style="margin-bottom:16px;">' +
            '<h4 style="color:#334155;">主要课程</h4>' +
            '<p style="color:#475569;">' + major.courses + '</p>' +
        '</div>' +
        '<div style="margin-bottom:16px;">' +
            '<h4 style="color:#334155;">就业方向</h4>' +
            '<p style="color:#475569;">' + major.careers + '</p>' +
        '</div>' +
        '<div style="background:#fefce8;padding:12px;border-radius:8px;text-align:center;">' +
            '<p style="color:#92400e;margin:0;">该专业适合霍兰德类型：' + typesStr + '</p>' +
        '</div>';

    document.getElementById('report-modal').classList.add('show');
}

// ==================== HOT MAJORS ====================
var currentHotTab = 'recent';

function switchHotTab(tab, btn) {
    currentHotTab = tab;
    document.querySelectorAll('#hot-tabs .tab').forEach(function(t) { t.classList.remove('active'); });
    btn.classList.add('active');
    renderHotContent();
}

function renderHotContent() {
    var container = document.getElementById('hot-content');
    if (currentHotTab === 'recent') {
        container.innerHTML = '<h3 style="margin-bottom:16px;color:#334155;">近三年最受考生追捧的热门专业 TOP 8</h3>' +
            hotMajorsRecent.map(function(m, i) {
                return '<div style="background:#f8fafc;border-radius:12px;padding:20px 24px;margin-bottom:16px;border-left:5px solid ' + m.color + ';">' +
                    '<div style="display:flex;align-items:center;gap:12px;margin-bottom:10px;">' +
                        '<span style="display:inline-flex;align-items:center;justify-content:center;width:48px;height:48px;border-radius:12px;background:' + m.color + ';color:white;font-weight:700;font-size:0.85rem;flex-shrink:0;">' + m.icon + '</span>' +
                        '<div>' +
                            '<h4 style="font-size:1.15rem;color:#1e293b;margin:0;">' + (i+1) + '. ' + m.name + ' <span style="background:' + m.color + ';color:white;padding:2px 10px;border-radius:12px;font-size:0.75rem;">' + m.rank + '</span></h4>' +
                            '<span style="font-size:0.85rem;color:var(--text-secondary);">' + m.category + '类</span>' +
                        '</div>' +
                    '</div>' +
                    '<p style="color:#475569;margin-bottom:8px;"><strong>热门原因：</strong>' + m.reason + '</p>' +
                    '<div style="display:flex;flex-wrap:wrap;gap:12px;margin-bottom:8px;">' +
                        '<span style="background:#eff6ff;color:#1e40af;padding:4px 12px;border-radius:8px;font-size:0.82rem;">' + m.salary + '</span>' +
                        '<span style="background:#fefce8;color:#92400e;padding:4px 12px;border-radius:8px;font-size:0.82rem;">' + m.trend + '</span>' +
                    '</div>' +
                    '<p style="color:#64748b;font-size:0.85rem;margin-bottom:4px;"><strong>推荐院校：</strong>' + m.schools + '</p>' +
                    '<p style="color:#0d9488;font-size:0.85rem;"><strong>报考建议：</strong>' + m.tips + '</p>' +
                '</div>';
            }).join('');
    } else if (currentHotTab === 'future') {
        container.innerHTML = '<h3 style="margin-bottom:16px;color:#334155;">未来3-5年最具潜力的新兴专业 TOP 8</h3>' +
            hotMajorsFuture.map(function(m, i) {
                return '<div style="background:#f8fafc;border-radius:12px;padding:20px 24px;margin-bottom:16px;border-left:5px solid ' + m.color + ';">' +
                    '<div style="display:flex;align-items:center;gap:12px;margin-bottom:10px;">' +
                        '<span style="display:inline-flex;align-items:center;justify-content:center;width:48px;height:48px;border-radius:12px;background:' + m.color + ';color:white;font-weight:700;font-size:0.85rem;flex-shrink:0;">' + m.icon + '</span>' +
                        '<div>' +
                            '<h4 style="font-size:1.15rem;color:#1e293b;margin:0;">' + (i+1) + '. ' + m.name + '</h4>' +
                            '<span style="font-size:0.85rem;color:var(--text-secondary);">' + m.category + '类</span>' +
                        '</div>' +
                    '</div>' +
                    '<p style="color:#475569;margin-bottom:8px;"><strong>未来前景：</strong>' + m.reason + '</p>' +
                    '<div style="display:flex;flex-wrap:wrap;gap:12px;margin-bottom:8px;">' +
                        '<span style="background:#eff6ff;color:#1e40af;padding:4px 12px;border-radius:8px;font-size:0.82rem;">' + m.salary + '</span>' +
                        '<span style="background:#dcfce7;color:#166534;padding:4px 12px;border-radius:8px;font-size:0.82rem;">' + m.growth + '</span>' +
                    '</div>' +
                    '<p style="color:#64748b;font-size:0.85rem;margin-bottom:4px;"><strong>推荐院校：</strong>' + m.schools + '</p>' +
                    '<p style="color:#8b5cf6;font-size:0.85rem;"><strong>关键词：</strong>' + m.keywords + '</p>' +
                '</div>';
            }).join('');
    } else if (currentHotTab === 'analysis') {
        container.innerHTML =
            '<h3 style="margin-bottom:16px;color:#334155;">高考专业选择趋势深度分析</h3>' +
            '<div style="background:linear-gradient(135deg,#eff6ff,#dbeafe);border-radius:12px;padding:24px;margin-bottom:20px;">' +
                '<h4 style="color:#1e40af;margin-bottom:12px;">近三年专业热度变化趋势</h4>' +
                '<div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:16px;">' +
                    '<div style="background:white;border-radius:10px;padding:16px;box-shadow:var(--shadow);">' +
                        '<h5 style="color:#6366f1;margin-bottom:8px;">持续上升</h5>' +
                        '<p style="color:#475569;font-size:0.9rem;">人工智能、集成电路、新能源、数据科学——受国家战略和产业升级驱动，录取分数连年攀升。</p>' +
                    '</div>' +
                    '<div style="background:white;border-radius:10px;padding:16px;box-shadow:var(--shadow);">' +
                        '<h5 style="color:#0d9488;margin-bottom:8px;">稳定热门</h5>' +
                        '<p style="color:#475569;font-size:0.9rem;">计算机类、临床医学、金融学、电气工程——就业面广、需求稳定，是历年的"常青树"专业。</p>' +
                    '</div>' +
                    '<div style="background:white;border-radius:10px;padding:16px;box-shadow:var(--shadow);">' +
                        '<h5 style="color:#f59e0b;margin-bottom:8px;">热度下降</h5>' +
                        '<p style="color:#475569;font-size:0.9rem;">传统土木建筑、部分管理类、纯外语类——受行业周期和AI冲击，报考热度有所回落。</p>' +
                    '</div>' +
                    '<div style="background:white;border-radius:10px;padding:16px;box-shadow:var(--shadow);">' +
                        '<h5 style="color:#ef4444;margin-bottom:8px;">正在转型</h5>' +
                        '<p style="color:#475569;font-size:0.9rem;">会计学、新闻传播、市场营销——传统方向遇冷，但"+科技"交叉方向（如智能财务、数据新闻）逆势增长。</p>' +
                    '</div>' +
                '</div>' +
            '</div>' +
            '<div style="background:linear-gradient(135deg,#fefce8,#fef3c7);border-radius:12px;padding:24px;margin-bottom:20px;">' +
                '<h4 style="color:#92400e;margin-bottom:12px;">未来5年专业选择核心逻辑</h4>' +
                '<ol style="color:#475569;line-height:2;">' +
                    '<li><strong>国家战略导向：</strong>芯片、新能源、人工智能是国家重点扶持领域，政策和资金持续倾斜，就业有保障。</li>' +
                    '<li><strong>人口结构变化：</strong>老龄化推动医疗健康、养老产业爆发；少子化提升对教育质量的要求。</li>' +
                    '<li><strong>技术革命驱动：</strong>AI不会取代所有工作，但"AI+专业"的复合型人才将成为最稀缺资源。</li>' +
                    '<li><strong>交叉学科崛起：</strong>生物+信息、金融+科技、艺术+技术等交叉领域是创新的主战场。</li>' +
                    '<li><strong>终身学习能力：</strong>专业只是起点，大学期间培养的自学能力、批判思维和适应力才是长期竞争力。</li>' +
                '</ol>' +
            '</div>' +
            '<div style="background:linear-gradient(135deg,#f0fdf4,#dcfce7);border-radius:12px;padding:24px;margin-bottom:20px;">' +
                '<h4 style="color:#166534;margin-bottom:12px;">给考生和家长的实用建议</h4>' +
                '<ul style="color:#475569;line-height:2;">' +
                    '<li><strong>兴趣优先：</strong>热门不等于适合。选择与自己兴趣和能力匹配的专业，才能在大学和职场保持长久动力。</li>' +
                    '<li><strong>关注交叉：</strong>建议选择有"+"方向的专业，如"计算机+金融"、"机械+AI"、"医学+工程"。</li>' +
                    '<li><strong>院校平台：</strong>好学校的平台资源（转专业、辅修、保研、实习机会）比单一专业选择更重要。</li>' +
                    '<li><strong>地域因素：</strong>高新产业集中在长三角、珠三角、京津冀、成渝等城市群，实习就业机会更多。</li>' +
                    '<li><strong>长远眼光：</strong>4年后的就业市场与今天可能大不相同，选择基础扎实、可拓展性强的专业更稳妥。</li>' +
                    '<li><strong>动态调整：</strong>大学期间可以通过辅修、跨专业考研、在线课程等方式调整方向，不要有"一选定终身"的焦虑。</li>' +
                '</ul>' +
            '</div>' +
            '<div style="text-align:center;padding:16px;background:#fef2f2;border-radius:12px;">' +
                '<p style="color:#dc2626;font-weight:600;font-size:0.95rem;">以上分析基于公开数据和行业趋势，仅供参考。具体志愿填报请结合个人情况和官方信息综合决策。</p>' +
            '</div>';
    }
}

// ==================== DOWNLOADS ====================
function renderDownloadGrid() {
    var grid = document.getElementById('download-grid');
    grid.innerHTML = downloadFiles.map(function(f) {
        return '<div class="download-card">' +
            '<div class="dl-icon ' + f.iconClass + '">' + f.iconText + '</div>' +
            '<h4>' + f.name + '</h4>' +
            '<p class="desc">' + f.desc + '</p>' +
            '<a href="' + f.url + '" target="_blank" rel="noopener noreferrer" class="btn btn-success btn-sm">下载试用版</a>' +
            '<span style="display:block;margin-top:10px;font-size:0.78rem;color:#dc2626;font-weight:600;">正式版需购买</span>' +
        '</div>';
    }).join('');
}

// ==================== MODAL CLICK OUTSIDE ====================
document.getElementById('report-modal').addEventListener('click', function(e) {
    if (e.target === this) closeReport();
});

// ==================== INIT ====================
function init() {
    renderQuestions();
    renderCategoryTabs();
    renderMajorList(majorsDB);
    renderDownloadGrid();
    renderHotContent();
}

init();
</script>

</body>
</html>
