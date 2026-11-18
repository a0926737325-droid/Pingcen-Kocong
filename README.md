<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>國中一年級阿美語（第七階第四課）線上情境圖文測驗</title>
<style>
  :root {
    --sky-top: #cbe7ff;
    --sky-mid: #eef7ff;
    --sky-bottom: #ffffff;
    --primary: #1e6091;
    --primary-light: #2b82c9;
    --accent: #f59e0b;
    --success: #16a34a;
    --danger: #dc2626;
    --text-main: #1e293b;
    --text-sub: #475569;
    --card-bg: rgba(255, 255, 255, 0.95);
  }

  * { box-sizing: border-box; font-family: "Microsoft JhengHei", "Noto Sans TC", sans-serif; }

  body {
    margin: 0;
    min-height: 100vh;
    background: linear-gradient(180deg, var(--sky-top) 0%, var(--sky-mid) 55%, var(--sky-bottom) 100%);
    color: var(--text-main);
    position: relative;
    overflow-x: hidden;
  }

  /* Decorative Clouds */
  .cloud {
    position: fixed;
    background: #fff;
    border-radius: 50px;
    opacity: 0.78;
    z-index: 0;
    pointer-events: none;
    box-shadow: 0 8px 20px rgba(30, 96, 145, 0.08);
  }
  .cloud::before, .cloud::after {
    content: '';
    position: absolute;
    background: #fff;
    border-radius: 50%;
  }
  .c1 { width: 160px; height: 50px; top: 40px; left: 6%; }
  .c1::before { width: 70px; height: 70px; top: -35px; left: 25px; }
  .c1::after { width: 55px; height: 55px; top: -25px; left: 80px; }

  .c2 { width: 200px; height: 60px; top: 110px; right: 8%; }
  .c2::before { width: 85px; height: 85px; top: -42px; left: 35px; }
  .c2::after { width: 65px; height: 65px; top: -30px; left: 105px; }

  .c3 { width: 140px; height: 44px; bottom: 80px; left: 10%; }
  .c3::before { width: 60px; height: 60px; top: -30px; left: 20px; }
  .c3::after { width: 48px; height: 48px; top: -20px; left: 70px; }

  .container {
    position: relative;
    z-index: 1;
    max-width: 920px;
    margin: 0 auto;
    padding: 28px 16px 60px;
  }

  header {
    text-align: center;
    background: var(--card-bg);
    border-radius: 20px;
    padding: 24px 20px;
    box-shadow: 0 10px 25px rgba(30, 96, 145, 0.12);
    border: 2px solid #bae6fd;
    margin-bottom: 22px;
  }

  header h1 {
    margin: 0 0 8px;
    font-size: 1.65rem;
    color: var(--primary);
  }

  header p {
    margin: 0;
    color: var(--text-sub);
    font-size: 1rem;
  }

  .quiz-panel {
    background: var(--card-bg);
    border-radius: 20px;
    padding: 28px;
    box-shadow: 0 10px 28px rgba(30, 96, 145, 0.1);
    border: 1px solid #e0f2fe;
  }

  h2.section-title {
    margin-top: 0;
    color: var(--primary);
    border-left: 6px solid var(--primary-light);
    padding-left: 12px;
    font-size: 1.3rem;
  }

  .student-bar {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 12px;
    background: #f8fafc;
    padding: 16px;
    border-radius: 12px;
    border: 1px solid #cbd5e1;
    margin-bottom: 22px;
  }
  .student-bar input {
    width: 100%;
    padding: 8px 10px;
    border: 1px solid #94a3b8;
    border-radius: 8px;
    font-size: 0.95rem;
    margin-top: 4px;
  }

  .q-block {
    background: #fff;
    border: 1px solid #e2e8f0;
    border-radius: 14px;
    padding: 16px 18px;
    margin-bottom: 14px;
  }
  .q-title { font-weight: bold; margin-bottom: 10px; font-size: 1.05rem; }

  .opt-label {
    display: block;
    padding: 9px 12px;
    margin: 6px 0;
    background: #f8fafc;
    border: 1px solid #cbd5e1;
    border-radius: 8px;
    cursor: pointer;
    transition: background 0.15s;
  }
  .opt-label:hover { background: #eff6ff; }
  .opt-label input { margin-right: 8px; }

  .word-bank-banner {
    background: #fffbeb;
    border: 2px dashed #f59e0b;
    padding: 12px;
    border-radius: 12px;
    text-align: center;
    font-weight: bold;
    color: #92400e;
    margin-bottom: 16px;
  }

  .fill-card {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 16px;
    background: #f8fafc;
    border: 1px solid #cbd5e1;
    border-radius: 14px;
    padding: 16px;
    margin-bottom: 14px;
  }
  .fill-visual {
    width: 96px;
    height: 96px;
    background: #fff;
    border-radius: 14px;
    border: 1px solid #e2e8f0;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    box-shadow: 0 3px 8px rgba(0,0,0,0.04);
  }
  .fill-body { flex: 1; min-width: 240px; }
  .fill-select {
    padding: 6px 10px;
    border-radius: 8px;
    border: 2px solid var(--primary-light);
    font-weight: bold;
    color: var(--primary);
    font-size: 1rem;
    background: #fff;
  }

  .feedback-tag {
    display: inline-block;
    margin-top: 8px;
    padding: 5px 12px;
    border-radius: 6px;
    font-size: 0.9rem;
    font-weight: bold;
  }
  .fb-ok { background: #dcfce7; color: #166534; }
  .fb-no { background: #fee2e2; color: #991b1b; }

  .action-btn {
    background: var(--primary);
    color: #fff;
    border: none;
    padding: 12px 28px;
    border-radius: 999px;
    font-size: 1.05rem;
    font-weight: bold;
    cursor: pointer;
    box-shadow: 0 4px 12px rgba(30, 96, 145, 0.25);
    transition: background 0.2s;
  }
  .action-btn:hover { background: var(--primary-light); }

  .reset-btn {
    background: #ffffff;
    color: var(--primary);
    padding: 12px 24px;
    border-radius: 999px;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    border: 2px solid #bae6fd;
    margin-left: 10px;
    transition: background 0.2s;
  }
  .reset-btn:hover { background: #f0f9ff; }

  .score-modal {
    display: none;
    margin-top: 24px;
    background: linear-gradient(135deg, #eff6ff, #dbeafe);
    border: 2px solid var(--primary);
    border-radius: 16px;
    padding: 22px;
    text-align: center;
  }
</style>
</head>
<body>

<div class="cloud c1"></div>
<div class="cloud c2"></div>
<div class="cloud c3"></div>

<div class="container">
  <header>
    <h1>🕒 國中一年級阿美語（第七階第四課）線上情境圖文測驗</h1>
    <p>課程主題：時鐘與時間（Tosa ko linom no toki.）｜共 15 題・滿分 100 分</p>
  </header>

  <main class="quiz-panel">
    <h2 class="section-title">學生基本資料</h2>
    <div class="student-bar">
      <div><label><strong>班級：</strong><input type="text" id="stu-class" placeholder="例如：701"></label></div>
      <div><label><strong>座號：</strong><input type="text" id="stu-num" placeholder="例如：12"></label></div>
      <div><label><strong>姓名：</strong><input type="text" id="stu-name" placeholder="請輸入姓名"></label></div>
    </div>

    <!-- Part 1: True/False -->
    <h3 style="color:var(--primary);">第一大題：是非題（每題 6 分，共 30 分）</h3>
    <div id="quiz-tf-container"></div>

    <!-- Part 2: Multiple Choice -->
    <h3 style="color:var(--primary); margin-top:26px;">第二大題：選擇題（每題 6 分，共 30 分）</h3>
    <div id="quiz-mc-container"></div>

    <!-- Part 3: Fill in the blank -->
    <h3 style="color:var(--primary); margin-top:26px;">第三大題：情境圖文填充題（每題 8 分，共 40 分）</h3>
    <div class="word-bank-banner">
      【參考詞庫】　tangasa　／　romi’ad　／　Harakatay　／　romakat　／　Matayo
    </div>
    <div id="quiz-fill-container"></div>

    <div style="text-align:center; margin-top:26px;">
      <button class="action-btn" onclick="gradeQuiz()">✅ 提交測驗並查看成績</button>
      <button class="reset-btn" onclick="resetQuiz()">🔄 清除重作</button>
    </div>

    <div id="score-modal" class="score-modal"></div>
  </main>
</div>

<script>
  // Quiz Data (15 Questions)
  const tfData = [
    { q: "1. 根據課文句型，當我們描述時鐘時，阿美語「Tosa ko linom no toki.」的意思是指「這個時鐘有兩個針（指針）」。", ans: "true", exp: "正確（○）：Tosa 是二，linom 是針，toki 是時鐘。" },
    { q: "2. 在課文詞彙中，「kakaya’ay」指的是「短的」，而「kamoko’ay」指的是「長的」。", ans: "false", exp: "錯誤（×）：剛好相反，kakaya’ay 是「長的」，kamoko’ay 是「短的」。" },
    { q: "3. 句子「Harakatay ko rakat no kakaya’ay a rinom.」的意思是「長的針走得比較快」。", ans: "true", exp: "正確（○）：Harakatay 意為比較快。" },
    { q: "4. 在描述時間流逝的句子中，「Nanodafak tangasa to dadaya」代表的意思是「從早上直到夜晚」。", ans: "true", exp: "正確（○）：Nanodafak 從早上，tangasa to dadaya 直到夜晚。" },
    { q: "5. 課文最後提到「Matiya kalimelaen ko romi’ad」，意思是「好像要珍惜日子那樣」。", ans: "true", exp: "正確（○）：kalimelaen ko romi’ad 意為珍惜日子。" }
  ];

  const mcData = [
    {
      q: "1. 在時鐘情境中，如果要表達「短的針走得比較慢」，阿美語應該怎麼說？",
      opts: [
        "(A) Harakatay ko rakat no kakaya’ay a rinom.",
        "(B) Matayo ko rakat no kamoko’ay a rinom.",
        "(C) Tosa ko linom no toki.",
        "(D) Nanodafak tangasa to dadaya."
      ],
      ans: 1,
      exp: "正確答案為 (B)：Matayo 為慢，kamoko’ay 為短的。"
    },
    {
      q: "2. 當我們看到時鐘的長針與短針時，課文中用來形容「長的和短的」詞組是哪一個？",
      opts: [
        "(A) O kakaya’ay ato kamoko’ay.",
        "(B) Harakatay ato matayo.",
        "(C) Nanodafak ato dadaya.",
        "(D) Kalimelaen ko romi’ad."
      ],
      ans: 0,
      exp: "正確答案為 (A)：O kakaya’ay ato kamoko’ay（長的和短的）。"
    },
    {
      q: "3. 句型中用來表達指針「不停止地走動」時，會使用哪一個詞組來形容其動作？",
      opts: [
        "(A) tangasa to dadaya",
        "(B) caay katomerep a romakat",
        "(C) sanay i kitaanan",
        "(D) tosa ko linom"
      ],
      ans: 1,
      exp: "正確答案為 (B)：caay katomerep a romakat（不停止地走動）。"
    },
    {
      q: "4. 關於時鐘指針的走動特性，下列哪一個阿美語詞彙是用來形容「比較快」的？",
      opts: [
        "(A) Matayo",
        "(B) Kamoko’ay",
        "(C) Harakatay",
        "(D) Kalimelaen"
      ],
      ans: 2,
      exp: "正確答案為 (C)：Harakatay（比較快的）。"
    },
    {
      q: "5. 在課文的總結句型中，教導我們應該如何看待每一天？",
      opts: [
        "(A) Tosa ko linom no toki",
        "(B) O kakaya’ay ato kamoko’ay",
        "(C) Matiya kalimelaen ko romi’ad",
        "(D) Caay katomerep a romakat"
      ],
      ans: 2,
      exp: "正確答案為 (C)：Matiya kalimelaen ko romi’ad（好像要珍惜日子那樣）。"
    }
  ];

  const fillData = [
    {
      svg: `<svg width="76" height="76" viewBox="0 0 100 100">
              <circle cx="50" cy="50" r="42" fill="#f0f9ff" stroke="#1e6091" stroke-width="5"/>
              <line x1="50" y1="50" x2="36" y2="42" stroke="#94a3b8" stroke-width="5" stroke-linecap="round"/>
              <line x1="50" y1="50" x2="76" y2="20" stroke="#dc2626" stroke-width="4" stroke-linecap="round"/>
              <path d="M72 34 A26 26 0 0 1 82 54" stroke="#dc2626" stroke-width="3" fill="none" stroke-dasharray="4,3"/>
            </svg>`,
      hint: "情境圖：紅色長針正在快速轉動（長的針走得比較快）",
      pre: "",
      post: " ko rakat no kakaya’ay a rinom.",
      ans: "Harakatay"
    },
    {
      svg: `<svg width="76" height="76" viewBox="0 0 100 100">
              <circle cx="50" cy="50" r="42" fill="#fffbeb" stroke="#1e6091" stroke-width="5"/>
              <line x1="50" y1="50" x2="72" y2="26" stroke="#94a3b8" stroke-width="3.5" stroke-linecap="round"/>
              <line x1="50" y1="50" x2="30" y2="46" stroke="#d97706" stroke-width="6" stroke-linecap="round"/>
            </svg>`,
      hint: "情境圖：橘色短針正在緩慢移動（短的針走得比較慢）",
      pre: "",
      post: " ko rakat no kamoko’ay a rinom.",
      ans: "Matayo"
    },
    {
      svg: `<svg width="76" height="76" viewBox="0 0 100 100">
              <circle cx="30" cy="34" r="15" fill="#f59e0b"/>
              <path d="M16 76 Q50 52 84 76" stroke="#1e6091" stroke-width="4" fill="none" stroke-dasharray="5,4"/>
              <path d="M72 22 A14 14 0 1 0 84 40 A11 11 0 1 1 72 22 Z" fill="#2563eb"/>
            </svg>`,
      hint: "情境圖：太陽升起到月亮高掛（從早上直到夜晚）",
      pre: "Nanodafak ",
      post: " to dadaya.",
      ans: "tangasa"
    },
    {
      svg: `<svg width="76" height="76" viewBox="0 0 100 100">
              <circle cx="50" cy="50" r="36" fill="none" stroke="#16a34a" stroke-width="5" stroke-dasharray="14,8"/>
              <polygon points="82,42 92,54 76,56" fill="#16a34a"/>
              <circle cx="50" cy="50" r="6" fill="#1e6091"/>
              <line x1="50" y1="50" x2="50" y2="26" stroke="#1e6091" stroke-width="4" stroke-linecap="round"/>
            </svg>`,
      hint: "情境圖：時鐘指針持續循環運轉、沒有停下（不停止地走動）",
      pre: "caay katomerep a ",
      post: ".",
      ans: "romakat"
    },
    {
      svg: `<svg width="76" height="76" viewBox="0 0 100 100">
              <rect x="22" y="24" width="56" height="54" rx="8" fill="#fff" stroke="#1e6091" stroke-width="4"/>
              <line x1="22" y1="40" x2="78" y2="40" stroke="#1e6091" stroke-width="4"/>
              <path d="M50 68 C42 60 36 55 36 49 A7 7 0 0 1 50 48 A7 7 0 0 1 64 49 C64 55 58 60 50 68 Z" fill="#ef4444"/>
            </svg>`,
      hint: "情境圖：日曆與愛心提醒我們把握光陰（好像要珍惜日子那樣）",
      pre: "Matiya kalimelaen ko ",
      post: ".",
      ans: "romi’ad"
    }
  ];

  const wordBankOpts = ["Harakatay", "Matayo", "tangasa", "romakat", "romi’ad"];

  function renderQuiz() {
    // Render TF
    const tfBox = document.getElementById('quiz-tf-container');
    tfBox.innerHTML = tfData.map((item, i) => `
      <div class="q-block">
        <div class="q-title">${item.q}</div>
        <label class="opt-label"><input type="radio" name="tf_${i}" value="true"> ⭕ 正確（○）</label>
        <label class="opt-label"><input type="radio" name="tf_${i}" value="false"> ❌ 錯誤（×）</label>
        <div id="fb_tf_${i}"></div>
      </div>
    `).join('');

    // Render MC
    const mcBox = document.getElementById('quiz-mc-container');
    mcBox.innerHTML = mcData.map((item, i) => `
      <div class="q-block">
        <div class="q-title">${item.q}</div>
        ${item.opts.map((opt, oi) => `
          <label class="opt-label"><input type="radio" name="mc_${i}" value="${oi}"> ${opt}</label>
        `).join('')}
        <div id="fb_mc_${i}"></div>
      </div>
    `).join('');

    // Render Fill
    const fillBox = document.getElementById('quiz-fill-container');
    fillBox.innerHTML = fillData.map((item, i) => `
      <div class="fill-card">
        <div class="fill-visual">${item.svg}</div>
        <div class="fill-body">
          <div style="font-size:0.95rem; color:var(--text-sub); margin-bottom:8px;"><strong>${i+1}.</strong> ${item.hint}</div>
          <div style="font-size:1.1rem; font-weight:bold;">
            ${item.pre}
            <select id="fill_${i}" class="fill-select">
              <option value="">-- 請選擇單詞 --</option>
              ${wordBankOpts.map(w => `<option value="${w}">${w}</option>`).join('')}
            </select>
            ${item.post}
          </div>
          <div id="fb_fill_${i}"></div>
        </div>
      </div>
    `).join('');
  }

  function gradeQuiz() {
    let score = 0;

    // Check TF (6 pts each)
    tfData.forEach((item, i) => {
      const sel = document.querySelector(`input[name="tf_${i}"]:checked`);
      const fb = document.getElementById(`fb_tf_${i}`);
      if (sel && sel.value === item.ans) {
        score += 6;
        fb.innerHTML = `<span class="feedback-tag fb-ok">✅ 答對！+6分｜${item.exp}</span>`;
      } else {
        fb.innerHTML = `<span class="feedback-tag fb-no">❌ 答錯！｜${item.exp}</span>`;
      }
    });

    // Check MC (6 pts each)
    mcData.forEach((item, i) => {
      const sel = document.querySelector(`input[name="mc_${i}"]:checked`);
      const fb = document.getElementById(`fb_mc_${i}`);
      if (sel && parseInt(sel.value) === item.ans) {
        score += 6;
        fb.innerHTML = `<span class="feedback-tag fb-ok">✅ 答對！+6分｜${item.exp}</span>`;
      } else {
        fb.innerHTML = `<span class="feedback-tag fb-no">❌ 答錯！｜${item.exp}</span>`;
      }
    });

    // Check Fill (8 pts each)
    fillData.forEach((item, i) => {
      const val = document.getElementById(`fill_${i}`).value;
      const fb = document.getElementById(`fb_fill_${i}`);
      if (val === item.ans) {
        score += 8;
        fb.innerHTML = `<span class="feedback-tag fb-ok">✅ 答對！+8分（正確單詞：${item.ans}）</span>`;
      } else {
        fb.innerHTML = `<span class="feedback-tag fb-no">❌ 答錯！正確答案應為：${item.ans}</span>`;
      }
    });

    const stuClass = document.getElementById('stu-class').value || "未填寫班級";
    const stuNum = document.getElementById('stu-num').value || "未填座號";
    const stuName = document.getElementById('stu-name').value || "同學";

    const modal = document.getElementById('score-modal');
    modal.style.display = 'block';
    modal.innerHTML = `
      <h3 style="margin-top:0; color:var(--primary); font-size:1.45rem;">🎉 測驗完成成績單</h3>
      <p style="font-size:1.05rem;"><strong>${stuClass} 班 ${stuNum} 號 ${stuName}</strong></p>
      <div style="font-size:2.4rem; font-weight:bold; color:${score >= 60 ? '#16a34a' : '#dc2626'}; margin:10px 0;">
        總得分：${score} 分
      </div>
      <p style="color:var(--text-sub); margin-bottom:0;">
        Matiya kalimelaen ko romi’ad!（好像要珍惜日子那樣，繼續加油喔！）
      </p>
    `;
    modal.scrollIntoView({ behavior: 'smooth' });
  }

  function resetQuiz() {
    renderQuiz();
    document.getElementById('score-modal').style.display = 'none';
  }

  // Initialize on load
  renderQuiz();
</script>
</body>
</html>
