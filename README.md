<html lang="zh-CN">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>注册协助服务</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    :root {
      --bg: #0d1117;
      --card: #161b22;
      --border: #21262d;
      --accent: #4fc3f7;
      --accent2: #a78bfa;
      --text: #e6edf3;
      --muted: #8b949e;
      --green: #3fb950;
    }
    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Noto Sans SC', sans-serif;
      font-weight: 300;
      min-height: 100vh;
    }

    /* ── Hero ── */
    .page-hero {
      text-align: center;
      padding: 56px 24px 40px;
      border-bottom: 1px solid var(--border);
    }
    .page-hero h1 {
      font-size: clamp(1.6rem, 4vw, 2.2rem);
      font-weight: 700;
      margin-bottom: 12px;
    }
    .notice {
      background: #1a2233;
      border: 1px solid #2d3a52;
      border-radius: 10px;
      padding: 16px 20px;
      max-width: 640px;
      margin: 20px auto 0;
      font-size: .88rem;
      color: var(--muted);
      line-height: 1.8;
      text-align: left;
    }
    .notice strong { color: var(--accent); }
    .flow {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 6px;
      margin-top: 10px;
      font-size: .84rem;
    }
    .flow-step {
      background: #21262d;
      border-radius: 6px;
      padding: 4px 10px;
      color: var(--text);
      white-space: nowrap;
    }
    .arrow { color: var(--accent); font-size: 1rem; }

    /* ── Main ── */
    main {
      max-width: 1100px;
      margin: 0 auto;
      padding: 40px 24px 80px;
    }

    /* ── Filter ── */
    .filter-bar {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 32px;
    }
    .filter-btn {
      padding: 6px 16px;
      border-radius: 20px;
      border: 1px solid var(--border);
      background: transparent;
      color: var(--muted);
      font-size: .82rem;
      cursor: pointer;
      font-family: inherit;
      transition: all .2s;
    }
    .filter-btn:hover, .filter-btn.active {
      border-color: var(--accent);
      color: var(--accent);
      background: rgba(79,195,247,.08);
    }

    /* ── Grid ── */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 16px;
    }

    .service-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
      transition: border-color .2s, transform .2s, box-shadow .2s;
      cursor: default;
    }
    .service-card:hover {
      border-color: var(--accent);
      transform: translateY(-3px);
      box-shadow: 0 8px 24px rgba(79,195,247,.1);
    }
    .card-img {
      width: 100%;
      aspect-ratio: 16/9;
      object-fit: cover;
      display: block;
      background: #1e2a3d;
    }
    .card-body {
      padding: 14px 16px;
    }
    .card-title {
      font-size: .88rem;
      font-weight: 500;
      color: var(--text);
      line-height: 1.5;
      margin-bottom: 8px;
    }
    .card-title .sub {
      display: block;
      font-size: .78rem;
      font-weight: 300;
      color: var(--muted);
      margin-top: 2px;
    }
    .card-price {
      font-size: .82rem;
      font-weight: 500;
      color: var(--green);
      background: rgba(63,185,80,.1);
      border: 1px solid rgba(63,185,80,.2);
      border-radius: 6px;
      padding: 3px 8px;
      display: inline-block;
    }
    .card-price.inquiry { color: var(--accent); background: rgba(79,195,247,.1); border-color: rgba(79,195,247,.2); }
    .card-price.free { color: #f0a500; background: rgba(240,165,0,.1); border-color: rgba(240,165,0,.2); }

    /* ── Footer ── */
    footer {
      text-align: center;
      padding: 32px 24px;
      border-top: 1px solid var(--border);
      font-size: .8rem;
      color: var(--muted);
    }

    @media (max-width: 480px) {
      .grid { grid-template-columns: repeat(2, 1fr); gap: 10px; }
      main { padding: 24px 14px 60px; }
    }
  </style>
</head>
<body>


<div class="page-hero">
  <h1>注册协助服务</h1>
  <div class="notice">
    <p>① 对应服务价格标记在下方，确认好可接受的价格后，通过 <strong>淘宝 / 闲鱼</strong> 平台交易。</p>
    <p style="margin-top:8px">② 服务流程：</p>
    <div class="flow">
      <span class="flow-step">确认价格</span>
      <span class="arrow">→</span>
      <span class="flow-step">联系博主-markzyanna</span>
      <span class="arrow">→</span>
      <span class="flow-step">确认可做</span>
      <span class="arrow">→</span>
      <span class="flow-step">拍下宝贝</span>
      <span class="arrow">→</span>
      <span class="flow-step">确认收货</span>
    </div>
  </div>
</div>

<main>
  <div class="filter-bar">
    <button class="filter-btn active" onclick="filter('all', this)">全部</button>
    <button class="filter-btn" onclick="filter('证券', this)">证券平台</button>
    <button class="filter-btn" onclick="filter('银行', this)">银行账户</button>
    <button class="filter-btn" onclick="filter('加密', this)">加密交易所</button>
    <button class="filter-btn" onclick="filter('电话卡', this)">电话卡</button>
    <button class="filter-btn" onclick="filter('钱包', this)">钱包支付</button>
    <button class="filter-btn" onclick="filter('文件', this)">文件证明</button>
  </div>

  <div class="grid" id="grid">
    <!-- Cards injected by JS -->
  </div>
</main>

<footer>本页内容仅供参考，不构成投资、法律或税务建议。请独立判断并自行承担风险。</footer>

<script>
const services = [
  { name: "英国 giffgaff", sub: "实体/eSIM卡 · 空卡可帮充", price: "最低80元", tag: "电话卡", img: "https://gbport.com/wp-content/uploads/2026/05/giffgaff.jpg" },
  { name: "美国嘉信理财", sub: "注册协助 · 不参与CRS", price: "300元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/12/嘉信证券-2.jpg" },
  { name: "美国第一证券", sub: "注册协助 · 不参与CRS", price: "300元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/12/第一证券.jpg" },
  { name: "香港胜利证券", sub: "Victory · 协助注册", price: "50元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/12/胜利证券.jpg" },
  { name: "香港 Club SIM", sub: "实体/eSIM · 保号6港币/年", price: "最低100元", tag: "电话卡", img: "https://gbport.com/wp-content/uploads/2026/02/ScreenShot_2026-02-02_072732_246.jpg" },
  { name: "美国必贝证券", sub: "注册协助 · 不参与CRS", price: "50元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/11/必贝.jpg" },
  { name: "Bybit 交易所", sub: "各区美元卡 · 注册协助", price: "50元", tag: "加密", img: "https://gbport.com/wp-content/uploads/2025/11/bybit-1.jpg" },
  { name: "港区 Coinbase", sub: "注册协助 · 地址包过", price: "50元", tag: "加密", img: "https://gbport.com/wp-content/uploads/2026/03/coinbase.jpg" },
  { name: "Uphold 交易所", sub: "配英国英镑卡 · 1%消费返现", price: "300元", tag: "加密", img: "https://gbport.com/wp-content/uploads/2026/02/uphold.jpg" },
  { name: "香港奕丰 / 英国 iFAST", sub: "银行账户", price: "80元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2025/12/ifast.jpg" },
  { name: "美国 KAST", sub: "电子钱包 · 虚拟美元账户", price: "200元", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2026/05/kast.jpg" },
  { name: "Kraken 海妖", sub: "交易所 · 注册协助", price: "80元", tag: "加密", img: "https://gbport.com/wp-content/uploads/2025/12/Kraken.jpg" },
  { name: "美国 Remitly", sub: "熊猫速汇平替 · 指导注册", price: "50元", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2025/12/remitly.jpg" },
  { name: "WISE 钱包", sub: "收入来源证明文件协助", price: "80元", tag: "文件", img: "https://gbport.com/wp-content/uploads/2025/11/wise-1.jpg" },
  { name: "WISE 钱包", sub: "地址证明文件协助", price: "50元", tag: "文件", img: "https://gbport.com/wp-content/uploads/2025/11/wise-1.jpg" },
  { name: "WISE 英国公户", sub: "成品号出售", price: "3000元", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2025/11/wise-1.jpg" },
  { name: "WISE 钱包", sub: "注册协助 · 余额代充代收", price: "详询", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2025/11/wise-1.jpg" },
  { name: "瑞士杜高斯贝", sub: "银行注册 · 充值协助", price: "50元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2025/12/杜高斯贝.jpg" },
  { name: "熊猫速汇", sub: "各区新人礼 · 免费派送", price: "限新人", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2025/12/熊猫速汇.jpg" },
  { name: "盈立证券", sub: "新加坡/香港 · 注册协助", price: "50元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/12/盈立证券.jpg" },
  { name: "香港致富证券", sub: "注册协助 · 送新人礼", price: "50元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/12/致富证券.jpg" },
  { name: "香港卓锐证券", sub: "ZR.COM · 注册协助", price: "50元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/12/卓锐证券.jpg" },
  { name: "全球通用证明", sub: "地址证明 · 资金证明", price: "80元", tag: "文件", img: "https://gbport.com/wp-content/uploads/2025/12/地址证明.jpg" },
  { name: "美国华美银行", sub: "客户经理担保 · 大陆见证开户", price: "2000元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2025/12/华美银行-1.jpg" },
  { name: "瑞士 SafePal / Fiat24", sub: "瑞士欧元账户银行卡", price: "80元", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2025/12/safepal、fiat24-1.jpg" },
  { name: "Softlare 卡片", sub: "老牌钱包 · 申请认证转运", price: "最低80元", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2026/06/softlare-logo.jpg" },
  { name: "英国 Yonder 卡", sub: "协助注册 · 银行卡转运", price: "最低150元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2025/12/yonder.jpg" },
  { name: "英国 ZOPA 银行", sub: "协助注册 · 银行卡转运", price: "700元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2026/04/zopa.jpg" },
  { name: "香港立桥证券", sub: "老牌立桥集团 · 注册协助", price: "50元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/12/立桥证券.jpg" },
  { name: "香港熊猫证券", sub: "操作如长桥般 · 注册协助", price: "100元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2025/12/熊猫证券.jpg" },
  { name: "Alipay HK", sub: "7折代收余额 · 1:1充值", price: "详询", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2025/12/alipayHK.jpg" },
  { name: "Trading212", sub: "UK/EU区带卡 · 注册协助", price: "最低300元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2026/01/trading212.jpg" },
  { name: "香港复星证券", sub: "协助注册", price: "50元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2026/01/星财富.jpg" },
  { name: "英国 Freetrade", sub: "伦交所免佣 · 注册协助", price: "50元", tag: "证券", img: "https://gbport.com/wp-content/uploads/2026/01/freetradel-1.jpg" },
  { name: "Bybit 欧洲区", sub: "欧洲区开卡 · 注册协助", price: "80元", tag: "加密", img: "https://gbport.com/wp-content/uploads/2026/01/bybitEU-1.jpg" },
  { name: "OKX EU 交易所", sub: "注册协助 · 带Visa虚拟卡", price: "150元", tag: "加密", img: "https://gbport.com/wp-content/uploads/2026/01/OKX-1.jpg" },
  { name: "SumUpPay 卡", sub: "带英国账户 · 消费返赠0.5%", price: "最低150元", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2026/01/ScreenShot_2026-01-24_121734_843-1.jpg" },
  { name: "Stripe 港区", sub: "国际收款平台 · 可嵌入网站", price: "最低150元", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2026/01/stripe.logo_.jpg" },
  { name: "英国 Lloyds", sub: "协助办理 · 银行卡转运", price: "700元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2026/05/Lloyds.jpg" },
  { name: "英国 Tide", sub: "商业账户 · 可开6虚拟卡", price: "300元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2026/02/tide.png" },
  { name: "Loqbox", sub: "协助设置 · 英国信用建立", price: "100元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2026/03/Loqbox.jpg" },
  { name: "海外仓库转运", sub: "英国个人住宅 · 协助运卡回国", price: "400元", tag: "文件", img: "https://gbport.com/wp-content/uploads/2026/03/转运仓.jpg" },
  { name: "英国 Monzo", sub: "数字银行注册 · 银行卡转运", price: "700元", tag: "银行", img: "https://gbport.com/wp-content/uploads/2026/03/Monzo-1.jpg" },
  { name: "香港711-CSL", sub: "实体/eSIM卡购买", price: "最低100元", tag: "电话卡", img: "https://gbport.com/wp-content/uploads/2026/04/CSL1.jpg" },
  { name: "渣打银行", sub: "存款50万3个月 · 远程办理", price: "免费协办", tag: "银行", img: "https://gbport.com/wp-content/uploads/2026/06/更明亮更顯眼！-渣打銀行啟用新LOGO-2.jpg" },
  { name: "美国 ITIN 申请", sub: "一手资质 · 认证公司办理", price: "详询", tag: "文件", img: "https://gbport.com/wp-content/uploads/2026/06/ITIN.jpg" },
  { name: "全球交易所公户", sub: "主流公户代开 · 协助验证", price: "详询", tag: "加密", img: "https://gbport.com/wp-content/uploads/2026/06/公户代开-1.jpg" },
  { name: "欧美英 Wise 公户", sub: "公户协助代开 · 协助验证", price: "详询", tag: "钱包", img: "https://gbport.com/wp-content/uploads/2026/06/wise公户.jpg" },
];

let currentFilter = 'all';

function priceClass(p) {
  if (p === '详询' || p === '详询报价') return 'inquiry';
  if (p === '限新人' || p === '免费协办') return 'free';
  return '';
}

function render(list) {
  const grid = document.getElementById('grid');
  grid.innerHTML = list.map(s => `
    <div class="service-card">
      <img class="card-img" src="${s.img}" alt="${s.name}" loading="lazy"
           onerror="this.style.display='none'">
      <div class="card-body">
        <div class="card-title">
          ${s.name}
          <span class="sub">${s.sub}</span>
        </div>
        <span class="card-price ${priceClass(s.price)}">${s.price}</span>
      </div>
    </div>
  `).join('');
}

function filter(tag, btn) {
  currentFilter = tag;
  document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  render(tag === 'all' ? services : services.filter(s => s.tag === tag));
}

// tag mapping for filter buttons
const tagMap = { '证券': '证券', '银行': '银行', '加密': '加密', '电话卡': '电话卡', '钱包': '钱包', '文件': '文件' };
render(services);
</script>
</body>
</html>
