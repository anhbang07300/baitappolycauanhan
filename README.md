[polymaster_n_t_p_tr_c_nghi_m_polymer_thptqg (1).html](https://github.com/user-attachments/files/35330346/polymaster_n_t_p_tr_c_nghi_m_polymer_thptqg.1.html)
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, viewport-fit=cover" />
  <title>PolyMaster - Ôn Tập & Trắc Nghiệm Polymer THPTQG</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
          },
          colors: {
            brand: {
              50: '#eef2ff',
              100: '#e0e7ff',
              500: '#6366f1',
              600: '#4f46e5',
              700: '#4338ca',
              900: '#312e81',
            }
          }
        }
      }
    };
  </script>
  <style>
    body {
      font-family: 'Inter', sans-serif;
      overflow-x: hidden;
      -webkit-tap-highlight-color: transparent;
      touch-action: manipulation;
    }
    .chem-eq {
      font-variant-numeric: tabular-nums;
      letter-spacing: 0.01em;
      font-size: clamp(0.75rem, 2.9vw, 0.875rem);
    }
    .chem-eq sub, .chem-text sub {
      font-size: 0.72em;
      line-height: 0;
      position: relative;
      vertical-align: baseline;
      bottom: -0.22em;
    }
    /* Ẩn thanh cuộn nhưng vẫn cho phép vuốt ngang mượt */
    .no-scrollbar::-webkit-scrollbar {
      display: none;
    }
    .no-scrollbar {
      -ms-overflow-style: none;
      scrollbar-width: none;
    }
    /* Hỗ trợ vùng an toàn trên iPhone/Android có tai thỏ & thanh cử chỉ đáy */
    .pb-safe-bottom {
      padding-bottom: calc(5.25rem + env(safe-area-inset-bottom, 0px));
    }
    .bottom-nav-safe {
      padding-bottom: max(0.35rem, env(safe-area-inset-bottom, 0px));
    }
    .sticky-next-safe {
      bottom: calc(4.35rem + env(safe-area-inset-bottom, 0px));
    }
    @media (min-width: 768px) {
      .pb-safe-bottom {
        padding-bottom: 4rem;
      }
      .sticky-next-safe {
        bottom: 1.25rem;
      }
    }
    /* Custom scrollbar cho desktop */
    ::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    ::-webkit-scrollbar-track {
      background: transparent;
    }
    ::-webkit-scrollbar-thumb {
      background: rgba(148, 163, 184, 0.4);
      border-radius: 9999px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: rgba(148, 163, 184, 0.7);
    }
    @keyframes shake {
      0%, 100% { transform: translateX(0); }
      20%, 60% { transform: translateX(-5px); }
      40%, 80% { transform: translateX(5px); }
    }
    .animate-shake {
      animation: shake 0.35s ease-in-out;
    }
    @keyframes popIn {
      0% { opacity: 0; transform: scale(0.97) translateY(6px); }
      100% { opacity: 1; transform: scale(1) translateY(0); }
    }
    .animate-pop {
      animation: popIn 0.22s ease-out forwards;
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-slate-950 dark:text-slate-100 min-h-screen overflow-x-hidden transition-colors duration-200 selection:bg-indigo-500 selection:text-white">

  <!-- HEADER GỌN NHẸ 1 DÒNG CHO MOBILE & ĐẦY ĐỦ CHO DESKTOP -->
  <header class="sticky top-0 z-30 bg-white/95 dark:bg-slate-900/95 backdrop-blur-md border-b border-slate-200 dark:border-slate-800 shadow-sm">
    <div class="max-w-6xl mx-auto px-3.5 sm:px-4 h-14 sm:h-16 flex items-center justify-between gap-2">
      <!-- Logo -->
      <div class="flex items-center gap-2.5 min-w-0">
        <div class="w-9 h-9 sm:w-10 sm:h-10 shrink-0 rounded-xl bg-gradient-to-br from-indigo-600 to-cyan-500 flex items-center justify-center text-white shadow-md shadow-indigo-500/20">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 sm:w-6 sm:h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
            <polygon points="12 2 21 7 21 17 12 22 3 17 3 7 12 2"></polygon>
            <circle cx="12" cy="12" r="3"></circle>
            <line x1="12" y1="2" x2="12" y2="9"></line>
            <line x1="21" y1="17" x2="14.6" y2="13.5"></line>
            <line x1="3" y1="17" x2="9.4" y2="13.5"></line>
          </svg>
        </div>
        <div class="truncate">
          <h1 class="text-base sm:text-xl font-extrabold tracking-tight bg-gradient-to-r from-indigo-600 to-cyan-600 dark:from-indigo-400 dark:to-cyan-400 bg-clip-text text-transparent truncate">
            PolyMaster <span class="text-xs sm:text-sm font-bold">THPTQG</span>
          </h1>
          <p class="text-[11px] text-slate-500 dark:text-slate-400 hidden md:block">Chinh phục Phương trình & Lý thuyết Polymer</p>
        </div>
      </div>

      <!-- Desktop Navigation Tabs (Ẩn trên Mobile < 768px) -->
      <nav class="hidden md:flex items-center bg-slate-100 dark:bg-slate-800 p-1 rounded-xl">
        <button onclick="switchTab('handbook')" data-tab="handbook" class="nav-tab-btn px-4 py-2 rounded-lg text-sm font-semibold transition-all flex items-center gap-1.5 bg-white dark:bg-slate-700 text-indigo-600 dark:text-indigo-300 shadow-sm">
          <span>📘</span> <span>Sổ tay</span>
        </button>
        <button onclick="switchTab('quiz')" data-tab="quiz" class="nav-tab-btn px-4 py-2 rounded-lg text-sm font-semibold transition-all flex items-center gap-1.5 text-slate-600 dark:text-slate-300 hover:text-slate-900 dark:hover:text-white">
          <span>🎯</span> <span>Trắc nghiệm</span>
        </button>
        <button onclick="switchTab('match')" data-tab="match" class="nav-tab-btn px-4 py-2 rounded-lg text-sm font-semibold transition-all flex items-center gap-1.5 text-slate-600 dark:text-slate-300 hover:text-slate-900 dark:hover:text-white">
          <span>🧩</span> <span>Ghép thẻ</span>
        </button>
        <button onclick="switchTab('stats')" data-tab="stats" class="nav-tab-btn px-4 py-2 rounded-lg text-sm font-semibold transition-all flex items-center gap-1.5 text-slate-600 dark:text-slate-300 hover:text-slate-900 dark:hover:text-white">
          <span>📊</span> <span>Thống kê</span>
        </button>
      </nav>

      <!-- Right Controls: Quick Streak + Dark Mode Toggle -->
      <div class="flex items-center gap-1.5 sm:gap-2 shrink-0">
        <button onclick="switchTab('stats')" class="px-2.5 py-1.5 rounded-xl bg-amber-50 dark:bg-amber-950/60 border border-amber-200/70 dark:border-amber-800/60 text-amber-700 dark:text-amber-300 text-xs font-bold flex items-center gap-1" title="Xem thống kê học tập">
          <span>🔥</span><span id="header-best-streak">0</span>
        </button>
        <button id="theme-toggle" onclick="toggleTheme()" aria-label="Chuyển giao diện Sáng/Tối" class="w-10 h-10 rounded-xl bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 dark:hover:bg-slate-700 transition-colors flex items-center justify-center active:scale-95">
          <svg id="sun-icon" class="w-5 h-5 hidden dark:block text-amber-400" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <circle cx="12" cy="12" r="5"></circle>
            <path d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"></path>
          </svg>
          <svg id="moon-icon" class="w-5 h-5 block dark:hidden text-slate-700" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path>
          </svg>
        </button>
      </div>
    </div>
  </header>

  <!-- BOTTOM NAVIGATION BAR CHUẨN MOBILE (< 768px) -->
  <nav aria-label="Điều hướng chính trên điện thoại" class="md:hidden fixed bottom-0 inset-x-0 z-40 bg-white/95 dark:bg-slate-900/95 backdrop-blur-lg border-t border-slate-200 dark:border-slate-800 shadow-[0_-4px_20px_rgba(0,0,0,0.06)] bottom-nav-safe">
    <div class="grid grid-cols-4 gap-1 px-1.5 pt-1">
      <button onclick="switchTab('handbook')" data-tab="handbook" class="nav-tab-btn min-h-[50px] rounded-xl flex flex-col items-center justify-center gap-0.5 text-indigo-600 dark:text-indigo-400 bg-indigo-50/80 dark:bg-indigo-950/60 font-bold transition-all active:scale-95">
        <span class="text-lg leading-none">📘</span>
        <span class="text-[11px] tracking-tight">Sổ tay</span>
      </button>
      <button onclick="switchTab('quiz')" data-tab="quiz" class="nav-tab-btn min-h-[50px] rounded-xl flex flex-col items-center justify-center gap-0.5 text-slate-500 dark:text-slate-400 font-semibold transition-all active:scale-95">
        <span class="text-lg leading-none">🎯</span>
        <span class="text-[11px] tracking-tight">Trắc nghiệm</span>
      </button>
      <button onclick="switchTab('match')" data-tab="match" class="nav-tab-btn min-h-[50px] rounded-xl flex flex-col items-center justify-center gap-0.5 text-slate-500 dark:text-slate-400 font-semibold transition-all active:scale-95">
        <span class="text-lg leading-none">🧩</span>
        <span class="text-[11px] tracking-tight">Ghép thẻ</span>
      </button>
      <button onclick="switchTab('stats')" data-tab="stats" class="nav-tab-btn min-h-[50px] rounded-xl flex flex-col items-center justify-center gap-0.5 text-slate-500 dark:text-slate-400 font-semibold transition-all active:scale-95 relative">
        <span class="text-lg leading-none">📊</span>
        <span class="text-[11px] tracking-tight">Thống kê</span>
        <span id="nav-wrong-badge" class="hidden absolute top-1.5 right-4 w-2 h-2 rounded-full bg-rose-500"></span>
      </button>
    </div>
  </nav>

  <!-- MAIN CONTAINER -->
  <main id="swipe-area" class="max-w-6xl mx-auto px-3 sm:px-4 pt-4 sm:pt-6 pb-safe-bottom">

    <!-- ========================================================= -->
    <!-- VIEW 1: SỔ TAY PHƯƠNG TRÌNH & LÝ THUYẾT NHANH              -->
    <!-- ========================================================= -->
    <section id="view-handbook" class="animate-pop">
      <!-- Intro & Filters -->
      <div class="bg-white dark:bg-slate-900 rounded-2xl p-4 sm:p-5 border border-slate-200 dark:border-slate-800 shadow-sm mb-4 sm:mb-6">
        <div class="flex flex-col md:flex-row md:items-center justify-between gap-3 mb-3.5">
          <div>
            <h2 class="text-lg sm:text-xl font-extrabold text-slate-900 dark:text-white flex items-center gap-2">
              <span class="text-indigo-600 dark:text-indigo-400">🧪</span> Sổ tay Phương trình Polymer
            </h2>
            <p class="text-xs sm:text-sm text-slate-500 dark:text-slate-400 mt-0.5">Tra cứu monomer, phương trình điều chế, ứng dụng & mẹo thi THPTQG.</p>
          </div>
          <!-- Search input: text-base (16px) tránh iOS tự động zoom khi focus -->
          <div class="relative w-full md:w-80">
            <input type="text" id="handbook-search" oninput="handleHandbookSearch()" placeholder="Tìm PE, PVC, nilon, ống nước..." class="w-full h-11 pl-10 pr-10 text-base sm:text-sm rounded-xl bg-slate-100 dark:bg-slate-800 border border-transparent focus:border-indigo-500 focus:bg-white dark:focus:bg-slate-900 focus:outline-none transition-all" />
            <svg class="w-4 h-4 text-slate-400 absolute left-3.5 top-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <circle cx="11" cy="11" r="8"></circle><line x1="21" y1="21" x2="16.65" y2="16.65"></line>
            </svg>
            <button id="handbook-clear-btn" onclick="clearHandbookSearch()" aria-label="Xóa tìm kiếm" class="hidden absolute right-2 top-1.5 w-8 h-8 rounded-lg text-slate-400 hover:text-slate-700 dark:hover:text-white flex items-center justify-center">
              ✕
            </button>
          </div>
        </div>

        <!-- Category Filter Pills: Thanh cuộn ngang mượt (Horizontal Scroll Snap) trên Mobile -->
        <div class="flex items-center gap-2 overflow-x-auto no-scrollbar snap-x snap-mandatory -mx-1 px-1 pb-0.5" id="handbook-filters">
          <button onclick="setHandbookFilter('all')" data-cat="all" class="hb-filter snap-start shrink-0 min-h-[40px] px-3.5 py-2 rounded-xl text-xs sm:text-sm font-bold bg-indigo-600 text-white shadow-sm transition-all active:scale-95">
            Tất cả (21)
          </button>
          <button onclick="setHandbookFilter('plastic')" data-cat="plastic" class="hb-filter snap-start shrink-0 min-h-[40px] px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 dark:hover:bg-slate-700 transition-all active:scale-95">
            1. Chất dẻo (6)
          </button>
          <button onclick="setHandbookFilter('fiber')" data-cat="fiber" class="hb-filter snap-start shrink-0 min-h-[40px] px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 dark:hover:bg-slate-700 transition-all active:scale-95">
            2. Tơ sợi (6)
          </button>
          <button onclick="setHandbookFilter('rubber')" data-cat="rubber" class="hb-filter snap-start shrink-0 min-h-[40px] px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 dark:hover:bg-slate-700 transition-all active:scale-95">
            3. Cao su (6)
          </button>
          <button onclick="setHandbookFilter('natural')" data-cat="natural" class="hb-filter snap-start shrink-0 min-h-[40px] px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 dark:hover:bg-slate-700 transition-all active:scale-95">
            4. Thiên nhiên (3)
          </button>
        </div>
      </div>

      <!-- Cards Grid: 1 cột trên mobile, 2 cột trên desktop -->
      <div id="handbook-grid" class="grid grid-cols-1 md:grid-cols-2 gap-3.5 sm:gap-4">
        <!-- Populated by JS -->
      </div>
    </section>

    <!-- ========================================================= -->
    <!-- VIEW 2: LUYỆN TẬP TRẮC NGHIỆM CHUYÊN SÂU                   -->
    <!-- ========================================================= -->
    <section id="view-quiz" class="hidden animate-pop">
      
      <!-- Quiz Setup Screen -->
      <div id="quiz-setup" class="max-w-2xl mx-auto bg-white dark:bg-slate-900 rounded-2xl p-4 sm:p-8 border border-slate-200 dark:border-slate-800 shadow-sm">
        <div class="text-center mb-5">
          <span class="inline-flex items-center justify-center w-12 h-12 sm:w-14 sm:h-14 rounded-2xl bg-indigo-100 dark:bg-indigo-950 text-indigo-600 dark:text-indigo-400 text-2xl mb-2.5">🎯</span>
          <h2 class="text-xl sm:text-2xl font-extrabold text-slate-900 dark:text-white">Luyện tập Trắc nghiệm Polymer</h2>
          <p class="text-xs sm:text-sm text-slate-500 dark:text-slate-400 mt-1">Ngân hàng <span id="total-bank-count" class="font-bold text-indigo-600 dark:text-indigo-400">36</span> câu hỏi chuẩn THPTQG kèm phương trình giải thích.</p>
        </div>

        <!-- Topic Selection: Chip lớn dễ bấm bằng ngón cái -->
        <div class="mb-5">
          <label class="block text-sm font-bold text-slate-700 dark:text-slate-200 mb-2">1. Chọn chuyên đề ôn tập:</label>
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-2.5" id="quiz-topic-options">
            <button type="button" onclick="selectQuizTopic('all')" data-topic="all" class="q-topic-btn min-h-[56px] p-3.5 rounded-xl border-2 border-indigo-600 bg-indigo-50/70 dark:bg-indigo-950/50 text-left transition-all flex items-center justify-between active:scale-[0.99]">
              <div>
                <div class="font-bold text-sm text-indigo-700 dark:text-indigo-300">🌟 Tổng hợp tất cả</div>
                <div class="text-xs text-slate-500 dark:text-slate-400">Bao quát 4 chuyên đề</div>
              </div>
              <span class="text-xs font-bold px-2.5 py-1 rounded-lg bg-indigo-200/70 dark:bg-indigo-900 text-indigo-800 dark:text-indigo-200" id="count-all">36 câu</span>
            </button>
            <button type="button" onclick="selectQuizTopic('plastic')" data-topic="plastic" class="q-topic-btn min-h-[56px] p-3.5 rounded-xl border-2 border-slate-200 dark:border-slate-800 hover:border-indigo-400 text-left transition-all flex items-center justify-between active:scale-[0.99]">
              <div>
                <div class="font-bold text-sm">🧴 Chất dẻo phổ biến</div>
                <div class="text-xs text-slate-500 dark:text-slate-400">PE, PP, PVC, PS, PMMA, PPF</div>
              </div>
              <span class="text-xs font-semibold px-2.5 py-1 rounded-lg bg-slate-100 dark:bg-slate-800" id="count-plastic">10 câu</span>
            </button>
            <button type="button" onclick="selectQuizTopic('fiber')" data-topic="fiber" class="q-topic-btn min-h-[56px] p-3.5 rounded-xl border-2 border-slate-200 dark:border-slate-800 hover:border-indigo-400 text-left transition-all flex items-center justify-between active:scale-[0.99]">
              <div>
                <div class="font-bold text-sm">🧵 Tơ sợi</div>
                <div class="text-xs text-slate-500 dark:text-slate-400">Thiên nhiên, tổng hợp, nhân tạo</div>
              </div>
              <span class="text-xs font-semibold px-2.5 py-1 rounded-lg bg-slate-100 dark:bg-slate-800" id="count-fiber">10 câu</span>
            </button>
            <button type="button" onclick="selectQuizTopic('rubber')" data-topic="rubber" class="q-topic-btn min-h-[56px] p-3.5 rounded-xl border-2 border-slate-200 dark:border-slate-800 hover:border-indigo-400 text-left transition-all flex items-center justify-between active:scale-[0.99]">
              <div>
                <div class="font-bold text-sm">🛞 Cao su</div>
                <div class="text-xs text-slate-500 dark:text-slate-400">Buna, Buna-S/N, lưu hóa</div>
              </div>
              <span class="text-xs font-semibold px-2.5 py-1 rounded-lg bg-slate-100 dark:bg-slate-800" id="count-rubber">9 câu</span>
            </button>
            <button type="button" onclick="selectQuizTopic('natural')" data-topic="natural" class="q-topic-btn min-h-[56px] p-3.5 rounded-xl border-2 border-slate-200 dark:border-slate-800 hover:border-indigo-400 text-left transition-all flex items-center justify-between sm:col-span-2 active:scale-[0.99]">
              <div>
                <div class="font-bold text-sm">🌿 Polymer thiên nhiên & Vận dụng</div>
                <div class="text-xs text-slate-500 dark:text-slate-400">Cellulose, Tinh bột, Protein & Đếm phát biểu</div>
              </div>
              <span class="text-xs font-semibold px-2.5 py-1 rounded-lg bg-slate-100 dark:bg-slate-800" id="count-natural">7 câu</span>
            </button>
          </div>
        </div>

        <!-- Question Count Selection: 3 nút lớn dễ chạm -->
        <div class="mb-6">
          <label class="block text-sm font-bold text-slate-700 dark:text-slate-200 mb-2">2. Số lượng câu hỏi:</label>
          <div class="grid grid-cols-3 gap-2.5" id="quiz-count-options">
            <button type="button" onclick="selectQuizCount(10)" data-count="10" class="q-count-btn min-h-[48px] py-2.5 rounded-xl border-2 border-indigo-600 bg-indigo-50/70 dark:bg-indigo-950/50 font-bold text-sm text-indigo-700 dark:text-indigo-300 transition-all active:scale-95">10 câu</button>
            <button type="button" onclick="selectQuizCount(20)" data-count="20" class="q-count-btn min-h-[48px] py-2.5 rounded-xl border-2 border-slate-200 dark:border-slate-800 font-semibold text-sm hover:border-indigo-400 transition-all active:scale-95">20 câu</button>
            <button type="button" onclick="selectQuizCount(999)" data-count="999" class="q-count-btn min-h-[48px] py-2.5 rounded-xl border-2 border-slate-200 dark:border-slate-800 font-semibold text-sm hover:border-indigo-400 transition-all active:scale-95">Tất cả</button>
          </div>
        </div>

        <button onclick="startQuiz()" class="w-full min-h-[52px] py-3.5 px-6 rounded-xl bg-gradient-to-r from-indigo-600 to-cyan-600 hover:from-indigo-700 hover:to-cyan-700 text-white font-bold text-base shadow-lg shadow-indigo-500/25 transition-all active:scale-[0.98] flex items-center justify-center gap-2">
          <span>Bắt đầu làm bài ngay</span>
          <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"></path></svg>
        </button>
      </div>

      <!-- Active Quiz Screen -->
      <div id="quiz-active" class="hidden max-w-3xl mx-auto">
        <!-- Top Status Bar dính gọn ở đầu trang dưới Header -->
        <div class="sticky top-14 sm:top-16 z-20 bg-white/95 dark:bg-slate-900/95 backdrop-blur-md rounded-2xl p-3 sm:p-4 border border-slate-200 dark:border-slate-800 shadow-sm mb-3.5">
          <div class="flex items-center justify-between text-xs sm:text-sm font-semibold mb-2">
            <div class="flex items-center gap-2">
              <button onclick="quitQuiz()" class="w-8 h-8 rounded-lg bg-slate-100 dark:bg-slate-800 text-slate-500 hover:text-rose-500 transition-colors flex items-center justify-center font-bold" title="Thoát bài làm">
                ✕
              </button>
              <span class="px-2.5 py-1 rounded-lg bg-indigo-100 dark:bg-indigo-950 text-indigo-700 dark:text-indigo-300 font-bold" id="quiz-progress-text">Câu 1 / 10</span>
              <span id="quiz-category-badge" class="hidden sm:inline-block px-2.5 py-1 rounded-lg bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300">Chất dẻo</span>
            </div>
            <div class="flex items-center gap-3">
              <span class="flex items-center gap-1 text-amber-500 font-bold" title="Chuỗi trả lời đúng liên tiếp">
                🔥 <span id="quiz-streak">0</span>
              </span>
              <span class="flex items-center gap-1 text-emerald-600 dark:text-emerald-400 font-bold">
                ✓ <span id="quiz-score">0</span>
              </span>
            </div>
          </div>
          <!-- Progress bar -->
          <div class="w-full h-2 bg-slate-100 dark:bg-slate-800 rounded-full overflow-hidden">
            <div id="quiz-progress-bar" class="h-full bg-gradient-to-r from-indigo-600 to-cyan-500 transition-all duration-300" style="width: 10%"></div>
          </div>
        </div>

        <!-- Question Card -->
        <div class="bg-white dark:bg-slate-900 rounded-2xl p-4 sm:p-7 border border-slate-200 dark:border-slate-800 shadow-sm">
          <div class="mb-2 flex items-center justify-between gap-2">
            <span id="quiz-difficulty-tag" class="text-[11px] font-bold uppercase tracking-wider px-2.5 py-0.5 rounded-md bg-cyan-100 dark:bg-cyan-950 text-cyan-700 dark:text-cyan-300">Nhận biết</span>
            <span id="quiz-mobile-cat" class="sm:hidden text-[11px] font-semibold text-slate-400">Chất dẻo</span>
          </div>
          <h3 id="quiz-question-text" class="chem-text text-[15px] sm:text-lg font-bold text-slate-900 dark:text-white leading-relaxed mb-4 sm:mb-5">
            <!-- Question text -->
          </h3>

          <!-- Options List: Nút bấm lớn padding 14-16px, khoảng cách 10px -->
          <div id="quiz-options" class="flex flex-col gap-2.5">
            <!-- Options buttons -->
          </div>

          <!-- Instant Feedback & Equation Explanation -->
          <div id="quiz-feedback" class="hidden mt-5 p-4 sm:p-5 rounded-2xl border transition-all animate-pop">
            <div class="flex items-center gap-2 font-extrabold text-sm sm:text-base mb-2" id="feedback-header">
              <!-- Correct / Wrong header -->
            </div>
            <div id="feedback-equation-box" class="my-2.5 p-3 rounded-xl bg-white/90 dark:bg-slate-950/80 border border-slate-200/80 dark:border-slate-800 font-mono text-indigo-700 dark:text-indigo-300 overflow-x-auto whitespace-nowrap chem-eq">
              <!-- Chemical equation -->
            </div>
            <p id="feedback-explanation" class="chem-text text-xs sm:text-sm text-slate-700 dark:text-slate-300 leading-relaxed">
              <!-- Detailed explanation -->
            </p>
          </div>
        </div>

        <!-- Nút Câu tiếp theo nổi bật ngay tầm tay dưới đáy màn hình -->
        <div id="quiz-next-wrap" class="hidden sticky sticky-next-safe z-20 mt-4">
          <button onclick="nextQuestion()" id="quiz-next-btn" class="w-full min-h-[52px] px-6 py-3.5 rounded-2xl bg-gradient-to-r from-indigo-600 to-cyan-600 hover:from-indigo-700 hover:to-cyan-700 text-white font-bold text-base shadow-xl shadow-indigo-600/30 transition-all active:scale-[0.98] flex items-center justify-center gap-2">
            <span>Câu tiếp theo</span>
            <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M9 5l7 7-7 7"></path></svg>
          </button>
        </div>
      </div>

      <!-- Quiz Result Summary Screen -->
      <div id="quiz-result" class="hidden max-w-2xl mx-auto bg-white dark:bg-slate-900 rounded-2xl p-5 sm:p-8 border border-slate-200 dark:border-slate-800 shadow-sm text-center animate-pop">
        <div id="result-emoji" class="text-5xl mb-3">🏆</div>
        <h2 class="text-xl sm:text-2xl font-extrabold text-slate-900 dark:text-white">Hoàn thành bài luyện tập!</h2>
        <p id="result-subtitle" class="text-xs sm:text-sm text-slate-500 dark:text-slate-400 mt-1 mb-5">Tuyệt vời! Bạn đã nắm rất vững kiến thức Polymer.</p>

        <div class="grid grid-cols-3 gap-2.5 sm:gap-3 mb-6">
          <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-800/70 border border-slate-100 dark:border-slate-800">
            <div class="text-[11px] sm:text-xs text-slate-500 dark:text-slate-400 font-medium">Điểm số</div>
            <div id="result-score-text" class="text-xl sm:text-2xl font-extrabold text-indigo-600 dark:text-indigo-400 mt-1">8/10</div>
          </div>
          <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-800/70 border border-slate-100 dark:border-slate-800">
            <div class="text-[11px] sm:text-xs text-slate-500 dark:text-slate-400 font-medium">Tỷ lệ đúng</div>
            <div id="result-accuracy" class="text-xl sm:text-2xl font-extrabold text-emerald-600 dark:text-emerald-400 mt-1">80%</div>
          </div>
          <div class="p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-800/70 border border-slate-100 dark:border-slate-800">
            <div class="text-[11px] sm:text-xs text-slate-500 dark:text-slate-400 font-medium">Chuỗi max</div>
            <div id="result-max-streak" class="text-xl sm:text-2xl font-extrabold text-amber-500 mt-1">5 🔥</div>
          </div>
        </div>

        <div class="flex flex-col sm:flex-row gap-2.5 justify-center">
          <button id="retry-wrong-btn" onclick="retryWrongQuestions()" class="hidden min-h-[48px] px-5 py-3 rounded-xl bg-amber-500 hover:bg-amber-600 text-white font-bold text-sm shadow-md transition-all active:scale-95 flex items-center justify-center gap-2">
            <span>🔁 Làm lại <span id="wrong-count-label">0</span> câu sai</span>
          </button>
          <button onclick="resetQuizToSetup()" class="min-h-[48px] px-5 py-3 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white font-bold text-sm shadow-md transition-all active:scale-95">
            Làm đề mới
          </button>
        </div>

        <!-- Review Wrong Answers List -->
        <div id="wrong-review-section" class="hidden mt-7 text-left border-t border-slate-200 dark:border-slate-800 pt-5">
          <h3 class="text-xs sm:text-sm font-bold uppercase tracking-wider text-rose-500 mb-3">Xem lại các câu cần lưu ý:</h3>
          <div id="wrong-review-list" class="space-y-3"></div>
        </div>
      </div>
    </section>

    <!-- ========================================================= -->
    <!-- VIEW 3: MINI-GAME GHÉP THẺ (TỐI ƯU MÀN HÌNH DỌC ĐIỆN THOẠI) -->
    <!-- ========================================================= -->
    <section id="view-match" class="hidden animate-pop">
      <div class="max-w-4xl mx-auto">
        <div class="bg-white dark:bg-slate-900 rounded-2xl p-4 sm:p-5 border border-slate-200 dark:border-slate-800 shadow-sm mb-4">
          <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3">
            <div>
              <h2 class="text-lg sm:text-xl font-extrabold text-slate-900 dark:text-white flex items-center gap-2">
                <span>🧩</span> Ghép cặp Nhanh Polymer
              </h2>
              <p class="text-xs sm:text-sm text-slate-500 dark:text-slate-400 mt-0.5">Chạm 1 thẻ ở nhóm trên (hoặc trái) và 1 thẻ tương ứng ở nhóm dưới (hoặc phải).</p>
            </div>

            <div class="flex items-center gap-2">
              <select id="match-mode-select" onchange="initMatchGame()" class="flex-1 sm:flex-none min-h-[44px] px-3 py-2 rounded-xl text-sm font-semibold bg-slate-100 dark:bg-slate-800 border border-slate-200 dark:border-slate-700 focus:outline-none focus:border-indigo-500">
                <option value="monomer">Monomer ↔ Polymer</option>
                <option value="application">Polymer ↔ Ứng dụng</option>
                <option value="reaction">Polymer ↔ Phân loại</option>
              </select>
              <button onclick="initMatchGame()" class="shrink-0 min-h-[44px] px-4 py-2 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white text-xs sm:text-sm font-bold shadow-sm transition-all active:scale-95">
                🔄 Đổi thẻ
              </button>
            </div>
          </div>
        </div>

        <!-- Game Stats Bar -->
        <div class="flex items-center justify-between px-4 py-2.5 mb-4 rounded-xl bg-indigo-50 dark:bg-indigo-950/50 border border-indigo-100 dark:border-indigo-900/60 text-xs sm:text-sm font-semibold">
          <span>Đã ghép: <strong id="match-progress" class="text-indigo-600 dark:text-indigo-400">0 / 5</strong></span>
          <span>Lượt thử: <strong id="match-attempts" class="text-slate-700 dark:text-slate-200">0</strong></span>
          <span>Thời gian: <strong id="match-timer" class="text-cyan-600 dark:text-cyan-400">00:00</strong></span>
        </div>

        <!-- Match Board: Mobile xếp 2 nhóm dọc (lưới 2 cột trong mỗi nhóm) để thẻ rộng rãi, không cắt chữ công thức; Desktop xếp 2 cột song song -->
        <div id="match-board" class="grid grid-cols-1 md:grid-cols-2 gap-4 sm:gap-5">
          <div class="bg-white/60 dark:bg-slate-900/50 p-3 rounded-2xl border border-indigo-200/70 dark:border-indigo-900/50">
            <div class="text-[11px] font-extrabold uppercase tracking-wider text-indigo-600 dark:text-indigo-400 mb-2 px-1" id="match-left-label">Nhóm 1 • Nguồn / Polymer</div>
            <div id="match-col-left" class="grid grid-cols-1 xs:grid-cols-2 md:grid-cols-1 gap-2.5"></div>
          </div>
          <div class="bg-white/60 dark:bg-slate-900/50 p-3 rounded-2xl border border-cyan-200/70 dark:border-cyan-900/50">
            <div class="text-[11px] font-extrabold uppercase tracking-wider text-cyan-600 dark:text-cyan-400 mb-2 px-1" id="match-right-label">Nhóm 2 • Sản phẩm / Đặc điểm</div>
            <div id="match-col-right" class="grid grid-cols-1 xs:grid-cols-2 md:grid-cols-1 gap-2.5"></div>
          </div>
        </div>

        <!-- Match Victory Banner -->
        <div id="match-victory" class="hidden mt-5 p-6 rounded-2xl bg-gradient-to-r from-emerald-500/10 to-cyan-500/10 border border-emerald-500/30 text-center animate-pop">
          <div class="text-4xl mb-2">🎉</div>
          <h3 class="text-lg font-extrabold text-emerald-700 dark:text-emerald-300">Xuất sắc! Bạn đã hoàn thành bảng ghép thẻ!</h3>
          <p id="match-victory-stats" class="text-sm text-slate-600 dark:text-slate-300 mt-1 mb-4"></p>
          <button onclick="initMatchGame()" class="min-h-[48px] px-6 py-2.5 rounded-xl bg-emerald-600 hover:bg-emerald-700 text-white font-bold text-sm shadow-md transition-all active:scale-95">
            Chơi ván mới
          </button>
        </div>
      </div>
    </section>

    <!-- ========================================================= -->
    <!-- VIEW 4: THỐNG KÊ TIẾN ĐỘ & KHO CÂU SAI (LƯU LOCALSTORAGE)  -->
    <!-- ========================================================= -->
    <section id="view-stats" class="hidden animate-pop">
      <div class="max-w-3xl mx-auto space-y-4">
        <div class="bg-white dark:bg-slate-900 rounded-2xl p-5 border border-slate-200 dark:border-slate-800 shadow-sm">
          <div class="flex items-center justify-between mb-4">
            <div>
              <h2 class="text-lg sm:text-xl font-extrabold text-slate-900 dark:text-white flex items-center gap-2">
                <span>📊</span> Thống kê Học tập của bạn
              </h2>
              <p class="text-xs sm:text-sm text-slate-500 dark:text-slate-400 mt-0.5">Dữ liệu được lưu tự động trên thiết bị này.</p>
            </div>
            <button onclick="confirmResetStats()" class="px-3 py-2 rounded-xl text-xs font-semibold text-rose-600 dark:text-rose-400 bg-rose-50 dark:bg-rose-950/50 hover:bg-rose-100 transition-colors">
              Đặt lại
            </button>
          </div>

          <div class="grid grid-cols-2 sm:grid-cols-4 gap-2.5 sm:gap-3">
            <div class="p-3.5 rounded-2xl bg-indigo-50/70 dark:bg-indigo-950/40 border border-indigo-100 dark:border-indigo-900/50">
              <div class="text-xs text-slate-500 dark:text-slate-400">Tổng câu đã làm</div>
              <div id="stat-total-answered" class="text-2xl font-extrabold text-indigo-600 dark:text-indigo-400 mt-1">0</div>
            </div>
            <div class="p-3.5 rounded-2xl bg-emerald-50/70 dark:bg-emerald-950/40 border border-emerald-100 dark:border-emerald-900/50">
              <div class="text-xs text-slate-500 dark:text-slate-400">Tỷ lệ chính xác</div>
              <div id="stat-accuracy-rate" class="text-2xl font-extrabold text-emerald-600 dark:text-emerald-400 mt-1">0%</div>
            </div>
            <div class="p-3.5 rounded-2xl bg-amber-50/70 dark:bg-amber-950/40 border border-amber-100 dark:border-amber-900/50">
              <div class="text-xs text-slate-500 dark:text-slate-400">Chuỗi đúng kỷ lục</div>
              <div id="stat-best-streak" class="text-2xl font-extrabold text-amber-500 mt-1">0 🔥</div>
            </div>
            <div class="p-3.5 rounded-2xl bg-rose-50/70 dark:bg-rose-950/40 border border-rose-100 dark:border-rose-900/50">
              <div class="text-xs text-slate-500 dark:text-slate-400">Câu sai cần ôn</div>
              <div id="stat-saved-wrong" class="text-2xl font-extrabold text-rose-600 dark:text-rose-400 mt-1">0</div>
            </div>
          </div>
        </div>

        <!-- Saved Wrong Questions Bank -->
        <div class="bg-white dark:bg-slate-900 rounded-2xl p-5 border border-slate-200 dark:border-slate-800 shadow-sm">
          <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 mb-4">
            <div>
              <h3 class="text-base sm:text-lg font-extrabold text-slate-900 dark:text-white">📌 Sổ tay Câu từng làm sai</h3>
              <p class="text-xs text-slate-500 dark:text-slate-400">Khi bạn làm đúng lại câu đó, hệ thống sẽ tự động gỡ khỏi danh sách này.</p>
            </div>
            <button id="practice-saved-wrong-btn" onclick="practiceSavedWrong()" class="hidden min-h-[44px] px-4 py-2 rounded-xl bg-amber-500 hover:bg-amber-600 text-white font-bold text-xs sm:text-sm shadow-sm transition-all active:scale-95">
              🎯 Ôn tập ngay các câu sai
            </button>
          </div>
          <div id="saved-wrong-list" class="space-y-3">
            <!-- Populated by JS -->
          </div>
        </div>
      </div>
    </section>

  </main>

  <!-- CUSTOM CONFIRM MODAL (KHÔNG DÙNG window.confirm) -->
  <div id="reset-modal" class="hidden fixed inset-0 z-50 bg-slate-950/60 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white dark:bg-slate-900 rounded-2xl max-w-sm w-full p-5 border border-slate-200 dark:border-slate-800 shadow-xl animate-pop">
      <h3 class="text-lg font-extrabold text-slate-900 dark:text-white mb-1.5">Đặt lại thống kê?</h3>
      <p class="text-sm text-slate-500 dark:text-slate-400 mb-5">Toàn bộ điểm tích lũy, chuỗi kỷ lục và danh sách câu sai đã lưu sẽ bị xóa.</p>
      <div class="flex gap-2.5 justify-end">
        <button onclick="closeResetModal()" class="min-h-[44px] px-4 py-2 rounded-xl bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-200 font-semibold text-sm">Hủy</button>
        <button onclick="executeResetStats()" class="min-h-[44px] px-4 py-2 rounded-xl bg-rose-600 text-white font-bold text-sm">Xóa dữ liệu</button>
      </div>
    </div>
  </div>

  <script>
    // =========================================================================
    // 1. DỮ LIỆU SỔ TAY POLYMER (21 POLYMER TRỌNG TÂM)
    // =========================================================================
    const HANDBOOK_DATA = [
      // --- 1. CHẤT DẺO ---
      {
        id: 'pe',
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        name: 'Polyethylene (PE)',
        monomer: 'Ethylene (CH₂=CH₂)',
        reactionType: 'Trùng hợp',
        equation: 'nCH₂=CH₂  —(t°, p, xt)→  (-CH₂-CH₂-)ₙ',
        applications: 'Làm túi nilon, màng bọc thực phẩm, chai lọ, bình chứa.',
        note: 'Chất dẻo mềm, không độc, cách điện tốt.'
      },
      {
        id: 'pp',
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        name: 'Polypropylene (PP)',
        monomer: 'Propylene (CH₂=CH-CH₃)',
        reactionType: 'Trùng hợp',
        equation: 'nCH₂=CH(CH₃)  —(t°, p, xt)→  (-CH₂-CH(CH₃)-)ₙ',
        applications: 'Làm bao bì, hộp đựng thực phẩm (chịu nhiệt tốt hơn PE), thừng, dây chão.',
        note: 'Bền cơ học hơn PE, chịu được nhiệt độ cao hơn.'
      },
      {
        id: 'pvc',
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        name: 'Poly(vinyl chloride) (PVC)',
        monomer: 'Vinyl chloride (CH₂=CH-Cl)',
        reactionType: 'Trùng hợp',
        equation: 'nCH₂=CHCl  —(t°, p, xt)→  (-CH₂-CHCl-)ₙ',
        applications: 'Làm ống dẫn nước, áo mưa, vỏ bọc dây điện, da giả, vật liệu xây dựng.',
        note: 'Chất rắn vô định hình, cách điện tốt, bền với axit.'
      },
      {
        id: 'ps',
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        name: 'Polystyrene (PS)',
        monomer: 'Styrene (C₆H₅-CH=CH₂)',
        reactionType: 'Trùng hợp',
        equation: 'nC₆H₅-CH=CH₂  —(t°, p, xt)→  (-CH₂-CH(C₆H₅)-)ₙ',
        applications: 'Làm hộp xốp đựng thức ăn, vỏ thiết bị điện tử (tivi, tủ lạnh), đồ gia dụng.',
        note: 'Nhựa nhiệt dẻo cứng, trong suốt, dễ gia công ép phun.'
      },
      {
        id: 'pmma',
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        name: 'Poly(methyl methacrylate) (PMMA)',
        monomer: 'Methyl methacrylate (CH₂=C(CH₃)-COOCH₃)',
        reactionType: 'Trùng hợp',
        equation: 'nCH₂=C(CH₃)COOCH₃  —(t°, p, xt)→  (-CH₂-C(CH₃)(COOCH₃)-)ₙ',
        applications: 'Thủy tinh hữu cơ (Plexiglas): làm kính máy bay, kính chống đạn, bể cá, bảng hiệu, kính bảo hộ.',
        note: 'Trong suốt, cho gần 90% ánh sáng truyền qua, không vỡ vụn sắc nhọn.'
      },
      {
        id: 'ppf',
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        name: 'Poly(phenol formaldehyde) (PPF)',
        monomer: 'Phenol (C₆H₅OH) & Formaldehyde (HCHO)',
        reactionType: 'Trùng ngưng',
        equation: 'nC₆H₅OH + nHCHO  —(H⁺/OH⁻, t°)→  Nhựa novolac / resol / rezit + nH₂O',
        applications: 'Nhựa bakelit: làm vỏ thiết bị cách điện, ổ cắm điện, tay cầm dụng cụ chịu nhiệt (xoong, chảo).',
        note: 'Nhựa rezit (bakelit) có cấu trúc mạng không gian, không nóng chảy, không tan.'
      },

      // --- 2. TƠ SỢI ---
      {
        id: 'to_thien_nhien',
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        name: 'Tơ thiên nhiên (Bông, Len, Tơ tằm)',
        monomer: 'Gốc β-glucose (bông) hoặc α-amino acid (len, tơ tằm)',
        reactionType: 'Có sẵn trong tự nhiên',
        equation: 'Bông: (C₆H₁₀O₅)ₙ  |  Len, Tơ tằm: (-NH-R-CO-)ₙ',
        applications: 'Dệt vải may mặc cao cấp, thoáng mát, thấm hút mồ hôi tốt.',
        note: 'Bông có bản chất cellulose; len (lông cừu) và tơ tằm có bản chất protein (kém bền trong kiềm/axit).'
      },
      {
        id: 'nylon6',
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        name: 'Tơ Nylon-6 (Tơ capron)',
        monomer: 'Caprolactam hoặc Axit ε-aminocaproic (H₂N-[CH₂]₅-COOH)',
        reactionType: 'Trùng hợp (vòng) hoặc Trùng ngưng',
        equation: 'nH₂N-[CH₂]₅-COOH  —(t°)→  (-NH-[CH₂]₅-CO-)ₙ + nH₂O',
        applications: 'Dệt vải may mặc, làm lưới đánh cá, dây cáp, chỉ khâu phẫu thuật.',
        note: 'Thuộc loại tơ polyamide (chứa nhóm -CO-NH-), kém bền với axit và kiềm.'
      },
      {
        id: 'nylon66',
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        name: 'Tơ Nylon-6,6',
        monomer: 'Hexamethylenediamine & Adipic acid',
        reactionType: 'Đồng trùng ngưng',
        equation: 'nH₂N-[CH₂]₆-NH₂ + nHOOC-[CH₂]₄-COOH  →  (-NH-[CH₂]₆-NH-CO-[CH₂]₄-CO-)ₙ + 2nH₂O',
        applications: 'Dệt vải lót săm lốp xe, bít tất, dây dù, bàn chải.',
        note: 'Tơ polyamide (mỗi mắt xích có 2 đoạn 6 cacbon nên gọi là nylon-6,6).'
      },
      {
        id: 'nitron',
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        name: 'Tơ Nitron (Tơ Olon)',
        monomer: 'Acrylonitrile (vinyl cyanide: CH₂=CH-CN)',
        reactionType: 'Trùng hợp',
        equation: 'nCH₂=CH-CN  —(t°, p, xt)→  (-CH₂-CH(CN)-)ₙ',
        applications: 'Dệt vải may quần áo ấm, bện thành sợi "len" đan áo rét.',
        note: 'Dai, bền với nhiệt và giữ nhiệt rất tốt. Được điều chế bằng phản ứng trùng hợp.'
      },
      {
        id: 'lapsan',
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        name: 'Tơ Lapsan (Terylene / PET)',
        monomer: 'Ethylene glycol & Terephthalic acid',
        reactionType: 'Đồng trùng ngưng',
        equation: 'nHO-CH₂-CH₂-OH + nHOOC-C₆H₄-COOH  →  (-O-CH₂-CH₂-O-CO-C₆H₄-CO-)ₙ + 2nH₂O',
        applications: 'Dệt vải may mặc chống nhăn, bền cơ học cao, chịu nhiệt.',
        note: 'Thuộc loại tơ polyester (chứa nhóm chức este -COO- trong mạch chính).'
      },
      {
        id: 'to_ban_tong_hop',
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        name: 'Tơ bán tổng hợp (Tơ Visco, Tơ Acetate)',
        monomer: 'Xuất phát từ polymer thiên nhiên: Cellulose',
        reactionType: 'Chế hóa hóa học từ polymer thiên nhiên',
        equation: 'Cellulose + CS₂/NaOH → Tơ visco  |  Cellulose + (CH₃CO)₂O → Tơ cellulose acetate',
        applications: 'Dệt vải may mặc mềm mại, óng mượt (vải lụa nhân tạo).',
        note: 'Còn gọi là tơ nhân tạo. Tuyệt đối KHÔNG nhầm tơ nhân tạo với tơ tổng hợp!'
      },

      // --- 3. CAO SU ---
      {
        id: 'caosu_thien_nhien',
        category: 'rubber',
        categoryLabel: 'Cao su',
        name: 'Cao su thiên nhiên',
        monomer: 'Isoprene (2-methylbuta-1,3-diene: CH₂=C(CH₃)-CH=CH₂)',
        reactionType: 'Có sẵn trong mủ cây cao su',
        equation: 'Cấu tạo polyisoprene dạng cis: (-CH₂-C(CH₃)=CH-CH₂-)ₙ',
        applications: 'Sản xuất săm lốp xe, găng tay y tế, đệm mút, dây chun.',
        note: 'Đàn hồi cao, không dẫn điện/nhiệt, không thấm khí và nước, tan trong xăng/benzen.'
      },
      {
        id: 'caosu_buna',
        category: 'rubber',
        categoryLabel: 'Cao su',
        name: 'Cao su Buna',
        monomer: 'Buta-1,3-diene (CH₂=CH-CH=CH₂)',
        reactionType: 'Trùng hợp (xúc tác Na)',
        equation: 'nCH₂=CH-CH=CH₂  —(Na, t°, p)→  (-CH₂-CH=CH-CH₂-)ₙ',
        applications: 'Chế tạo lốp xe, băng tải, ống dẫn.',
        note: 'Tính đàn hồi và độ bền kém hơn cao su thiên nhiên.'
      },
      {
        id: 'caosu_isoprene',
        category: 'rubber',
        categoryLabel: 'Cao su',
        name: 'Cao su Isoprene',
        monomer: 'Isoprene (CH₂=C(CH₃)-CH=CH₂)',
        reactionType: 'Trùng hợp (xúc tác đặc biệt)',
        equation: 'nCH₂=C(CH₃)-CH=CH₂  —(xt, t°, p)→  (-CH₂-C(CH₃)=CH-CH₂-)ₙ',
        applications: 'Thay thế cao su thiên nhiên làm lốp ô tô, thiết bị kỹ thuật.',
        note: 'Có cấu trúc và tính chất gần giống cao su thiên nhiên nhất.'
      },
      {
        id: 'caosu_chloroprene',
        category: 'rubber',
        categoryLabel: 'Cao su',
        name: 'Cao su Chloroprene',
        monomer: 'Chloroprene (2-chlorobuta-1,3-diene: CH₂=C(Cl)-CH=CH₂)',
        reactionType: 'Trùng hợp',
        equation: 'nCH₂=C(Cl)-CH=CH₂  —(xt, t°, p)→  (-CH₂-C(Cl)=CH-CH₂-)ₙ',
        applications: 'Làm ống dẫn dầu, vỏ bọc cáp điện, đồ lặn, băng tải chống cháy.',
        note: 'Bền với dầu mỡ, hóa chất và khó cháy hơn cao su thường nhờ chứa nguyên tử Cl.'
      },
      {
        id: 'caosu_buna_sn',
        category: 'rubber',
        categoryLabel: 'Cao su',
        name: 'Cao su Buna-S và Cao su Buna-N',
        monomer: 'Buta-1,3-diene + Styrene (Buna-S) hoặc + Acrylonitrile (Buna-N)',
        reactionType: 'Đồng trùng hợp',
        equation: 'Buta-1,3-diene + C₆H₅CH=CH₂ → Buna-S  |  Buta-1,3-diene + CH₂=CH-CN → Buna-N',
        applications: 'Buna-S: lốp xe (đàn hồi cao). Buna-N: gioăng cao su, ống dẫn xăng dầu (chống dầu cực tốt).',
        note: 'Chữ S là Styrene; chữ N là Nitron (acrylonitrile).'
      },
      {
        id: 'caosu_luu_hoa',
        category: 'rubber',
        categoryLabel: 'Cao su',
        name: 'Cao su lưu hóa',
        monomer: 'Cao su thô (thiên nhiên/tổng hợp) + Lưu huỳnh (S)',
        reactionType: 'Phản ứng khâu mạch (tăng mạch cacbon)',
        equation: 'Mạch polyisoprene + S  —(t°)→  Mạng không gian có cầu nối disulfide (-S-S-)',
        applications: 'Chế tạo lốp ô tô, máy bay, đế giày chịu mài mòn.',
        note: 'Cấu trúc mạng không gian giúp tăng độ bền cơ học, độ đàn hồi, chịu nhiệt và lâu mòn.'
      },

      // --- 4. POLYMER THIÊN NHIÊN KHÁC ---
      {
        id: 'cellulose',
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        name: 'Cellulose',
        monomer: 'Các gốc β-glucose liên kết β-1,4-glycoside',
        reactionType: 'Polymer thiên nhiên (quang hợp ở thực vật)',
        equation: '[C₆H₇O₂(OH)₃]ₙ  (Mạch không phân nhánh)',
        applications: 'Thành phần chính của gỗ, bông, đay, gai; sản xuất giấy, tơ nhân tạo (visco, acetate).',
        note: 'Cấu trúc mạch không phân nhánh, không tan trong nước, tan trong nước Schweizer.'
      },
      {
        id: 'tinh_bot',
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        name: 'Tinh bột (Amylose & Amylopectin)',
        monomer: 'Các gốc α-glucose',
        reactionType: 'Polymer thiên nhiên (quang hợp ở thực vật)',
        equation: '(C₆H₁₀O₅)ₙ : Amylose (mạch không nhánh) + Amylopectin (mạch phân nhánh)',
        applications: 'Nguồn lương thực chính (gạo, ngô, khoai, sắn), sản xuất bánh kẹo, ethanol.',
        note: 'Amylose xoắn lò xo nhờ liên kết hydrogen; amylopectin có mạch phân nhánh (α-1,4 và α-1,6).'
      },
      {
        id: 'protein',
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        name: 'Protein',
        monomer: 'Các gốc α-amino acid liên kết bằng liên kết peptide (-CO-NH-)',
        reactionType: 'Polymer thiên nhiên (sinh tổng hợp trong cơ thể sống)',
        equation: 'Chuỗi polypeptide: (-NH-CH(R)-CO-)ₙ',
        applications: 'Cấu tạo nên cơ, da, tóc, móng, sừng, tơ tằm, enzyme xúc tác sinh học.',
        note: 'Bị đông tụ khi đun nóng hoặc gặp axit/kiềm; thủy phân hoàn toàn thu được các α-amino acid.'
      }
    ];

    // =========================================================================
    // 2. NGÂN HÀNG 36 CÂU HỎI TRẮC NGHIỆM CHUYÊN SÂU THPTQG
    // =========================================================================
    const QUIZ_BANK = [
      // --- CHẤT DẺO (10 câu) ---
      {
        id: 1,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Nhận biết',
        question: 'Poly(vinyl chloride) (PVC) dùng để sản xuất ống dẫn nước, áo mưa, vỏ bọc dây điện được điều chế bằng phản ứng trùng hợp monomer nào sau đây?',
        options: [
          'CH₂=CH-Cl',
          'CH₂=CH₂',
          'CH₂=CH-CH₃',
          'C₆H₅-CH=CH₂'
        ],
        answer: 0,
        equation: 'nCH₂=CH-Cl  —(t°, p, xt)→  (-CH₂-CHCl-)ₙ',
        explanation: 'Vinyl chloride (CH₂=CH-Cl) tham gia phản ứng trùng hợp tạo thành poly(vinyl chloride), viết tắt là PVC.'
      },
      {
        id: 2,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Nhận biết',
        question: 'Polymer nào sau đây được dùng để chế tạo "thủy tinh hữu cơ" (Plexiglas) ứng dụng làm kính máy bay, kính chống đạn, bể cá?',
        options: [
          'Poly(methyl methacrylate)',
          'Poly(phenol formaldehyde)',
          'Polystyrene',
          'Polypropylene'
        ],
        answer: 0,
        equation: 'nCH₂=C(CH₃)-COOCH₃  —(t°, p, xt)→  (-CH₂-C(CH₃)(COOCH₃)-)ₙ',
        explanation: 'Poly(methyl methacrylate) (PMMA) rất trong suốt, cho ánh sáng truyền qua tốt và bền va đập nên được gọi là thủy tinh hữu cơ.'
      },
      {
        id: 3,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Thông hiểu',
        question: 'Trong các chất dẻo sau, polymer nào được điều chế bằng phản ứng trùng ngưng?',
        options: [
          'Poly(phenol formaldehyde) (PPF)',
          'Polyethylene (PE)',
          'Polystyrene (PS)',
          'Poly(methyl methacrylate) (PMMA)'
        ],
        answer: 0,
        equation: 'nC₆H₅OH + nHCHO  —(H⁺/OH⁻, t°)→  Nhựa PPF + nH₂O',
        explanation: 'PPF (nhựa bakelit) được tạo thành từ phản ứng trùng ngưng giữa phenol và formaldehyde (có giải phóng phân tử H₂O). Các chất còn lại đều là trùng hợp.'
      },
      {
        id: 4,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Nhận biết',
        question: 'Hộp xốp đựng thức ăn, vỏ thiết bị điện tử (tivi, máy tính) thường được sản xuất từ polymer nào dưới đây?',
        options: [
          'Polystyrene (PS)',
          'Poly(vinyl chloride) (PVC)',
          'Poly(phenol formaldehyde) (PPF)',
          'Polyethylene (PE)'
        ],
        answer: 0,
        equation: 'nC₆H₅-CH=CH₂  —(t°, p, xt)→  (-CH₂-CH(C₆H₅)-)ₙ',
        explanation: 'Polystyrene (PS) được điều chế từ styrene (C₆H₅-CH=CH₂), dùng phổ biến để làm hộp xốp cách nhiệt và vỏ đồ điện tử.'
      },
      {
        id: 5,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Thông hiểu',
        question: 'Tay cầm của xoong, chảo chịu nhiệt và vỏ ổ cắm điện cách điện thường được làm từ loại nhựa nào?',
        options: [
          'Nhựa bakelit (Poly(phenol formaldehyde))',
          'Nhựa PE (Polyethylene)',
          'Nhựa PS (Polystyrene)',
          'Nhựa PMMA (Thủy tinh hữu cơ)'
        ],
        answer: 0,
        equation: 'Phenol + Formaldehyde  —(t°, xt)→  Nhựa rezit (bakelit)',
        explanation: 'Nhựa bakelit (dạng rezit của PPF) có cấu trúc mạng không gian nên bền nhiệt, không nóng chảy và cách điện cực tốt.'
      },
      {
        id: 6,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Nhận biết',
        question: 'Monomer dùng để điều chế nhựa PP (Polypropylene) làm bao bì, hộp đựng thực phẩm, dây chão là:',
        options: [
          'CH₂=CH-CH₃',
          'CH₂=CH₂',
          'CH₂=C(CH₃)₂',
          'CH₂=CH-CN'
        ],
        answer: 0,
        equation: 'nCH₂=CH-CH₃  —(t°, p, xt)→  (-CH₂-CH(CH₃)-)ₙ',
        explanation: 'Propylene (propene: CH₂=CH-CH₃) trùng hợp tạo thành polypropylene (PP).'
      },
      {
        id: 7,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Thông hiểu',
        question: 'Cho sơ đồ chuyển hóa: CH₄ → X → Y → PVC. Hai chất X và Y lần lượt là:',
        options: [
          'C₂H₂ và CH₂=CH-Cl',
          'C₂H₄ và CH₂=CH-Cl',
          'C₂H₂ và CH₃-CH₂Cl',
          'C₂H₆ và CH₂=CH₂'
        ],
        answer: 0,
        equation: '2CH₄ —(1500°C, làm lạnh nhanh)→ C₂H₂ + 3H₂  ;  C₂H₂ + HCl —(HgCl₂, t°)→ CH₂=CH-Cl',
        explanation: 'Từ CH₄ nhiệt phân nhanh ở 1500°C thu được acetylene (X: C₂H₂). Cộng HCl tỉ lệ 1:1 thu được vinyl chloride (Y: CH₂=CH-Cl), sau đó trùng hợp ra PVC.'
      },
      {
        id: 8,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Vận dụng',
        question: 'Một đoạn mạch PVC có phân tử khối trung bình là 750.000 đvC. Hệ số polymer hóa (n) của đoạn mạch PVC này là:',
        options: [
          '12.000',
          '15.000',
          '10.000',
          '26.785'
        ],
        answer: 0,
        equation: 'M(mắt xích -CH₂-CHCl-) = 12×2 + 3 + 35,5 = 62,5  ⇒  n = 750.000 / 62,5 = 12.000',
        explanation: 'Mắt xích của PVC là -C₂H₃Cl- có M = 62,5. Lấy phân tử khối polymer chia cho 62,5 ta được n = 12.000.'
      },
      {
        id: 9,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Thông hiểu',
        question: 'Túi nilon, màng bọc thực phẩm phổ biến nhất hiện nay được sản xuất chủ yếu từ polymer nào?',
        options: [
          'Polyethylene (PE)',
          'Poly(vinyl chloride) (PVC)',
          'Poly(phenol formaldehyde) (PPF)',
          'Polystyrene (PS)'
        ],
        answer: 0,
        equation: 'nCH₂=CH₂  —(t°, p, xt)→  (-CH₂-CH₂-)ₙ',
        explanation: 'PE mềm dẻo, không độc hại, dễ thổi màng mỏng nên dùng làm túi nilon và màng bọc thực phẩm.'
      },
      {
        id: 10,
        category: 'plastic',
        categoryLabel: 'Chất dẻo',
        difficulty: 'Thông hiểu',
        question: 'Methyl methacrylate là monomer dùng để điều chế PMMA. Công thức cấu tạo thu gọn của methyl methacrylate là:',
        options: [
          'CH₂=C(CH₃)-COOCH₃',
          'CH₂=CH-COOCH₃',
          'CH₃-COO-CH=CH₂',
          'CH₂=C(CH₃)-COOH'
        ],
        answer: 0,
        equation: 'nCH₂=C(CH₃)-COOCH₃  —(t°, p, xt)→  PMMA',
        explanation: 'Methyl methacrylate là este của methyl alcohol (CH₃OH) và methacrylic acid (CH₂=C(CH₃)-COOH).'
      },

      // --- TƠ SỢI (10 câu) ---
      {
        id: 11,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Nhận biết',
        question: 'Loại tơ nào sau đây thuộc loại tơ bán tổng hợp (tơ nhân tạo)?',
        options: [
          'Tơ visco và tơ cellulose acetate',
          'Tơ capron và tơ nylon-6,6',
          'Tơ tằm và len',
          'Tơ nitron và tơ lapsan'
        ],
        answer: 0,
        equation: 'Cellulose (tự nhiên)  —(chế hóa hóa học)→  Tơ visco / Tơ cellulose acetate',
        explanation: 'Tơ bán tổng hợp (nhân tạo) xuất phát từ polymer thiên nhiên (cellulose) rồi chế hóa thêm bằng phương pháp hóa học.'
      },
      {
        id: 12,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Nhận biết',
        question: 'Tơ nitron (tơ olon) bền với nhiệt và giữ nhiệt tốt nên thường được dùng để dệt vải may quần áo ấm. Monomer tạo ra tơ nitron là:',
        options: [
          'Acrylonitrile (CH₂=CH-CN)',
          'Caprolactam',
          'Vinyl acetate (CH₃COOCH=CH₂)',
          'Methyl methacrylate'
        ],
        answer: 0,
        equation: 'nCH₂=CH-CN  —(t°, p, xt)→  (-CH₂-CH(CN)-)ₙ',
        explanation: 'Tơ nitron (olon) được điều chế bằng phản ứng TRÙNG HỢP acrylonitrile (vinyl cyanide).'
      },
      {
        id: 13,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Thông hiểu',
        question: 'Tơ nylon-6,6 được điều chế bằng phản ứng đồng trùng ngưng giữa hai monomer nào sau đây?',
        options: [
          'Hexamethylenediamine và adipic acid',
          'Ethylene glycol và terephthalic acid',
          'Hexamethylenediamine và terephthalic acid',
          'Ethylene glycol và adipic acid'
        ],
        answer: 0,
        equation: 'nH₂N-[CH₂]₆-NH₂ + nHOOC-[CH₂]₄-COOH  →  (-NH-[CH₂]₆-NH-CO-[CH₂]₄-CO-)ₙ + 2nH₂O',
        explanation: 'Hexamethylenediamine có 6 nguyên tử C và adipic acid cũng có 6 nguyên tử C, đồng trùng ngưng tạo ra nylon-6,6.'
      },
      {
        id: 14,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Thông hiểu',
        question: 'Tơ lapsan thuộc loại tơ polyester, được điều chế từ ethylene glycol và axit nào sau đây?',
        options: [
          'Terephthalic acid (p-HOOC-C₆H₄-COOH)',
          'Adipic acid (HOOC-[CH₂]₄-COOH)',
          'Acrylic acid (CH₂=CH-COOH)',
          'Acetic acid (CH₃COOH)'
        ],
        answer: 0,
        equation: 'nHO-CH₂-CH₂-OH + nHOOC-C₆H₄-COOH  →  (-O-CH₂-CH₂-O-CO-C₆H₄-CO-)ₙ + 2nH₂O',
        explanation: 'Đồng trùng ngưng ethylene glycol và terephthalic acid thu được poly(ethylene terephthalate) dùng kéo sợi gọi là tơ lapsan.'
      },
      {
        id: 15,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Thông hiểu',
        question: 'Trong các loại tơ sau: (1) tơ tằm, (2) tơ capron, (3) tơ nitron, (4) tơ nylon-6,6. Những loại tơ thuộc nhóm tơ polyamide (kém bền trong môi trường axit/kiềm) là:',
        options: [
          '(1), (2), (4)',
          '(2), (3), (4)',
          '(1), (2), (3)',
          '(2), (4)'
        ],
        answer: 0,
        equation: 'Liên kết -CO-NH- bị thủy phân trong dung dịch axit hoặc kiềm đun nóng.',
        explanation: 'Tơ tằm (protein), tơ capron (nylon-6) và tơ nylon-6,6 đều chứa nhiều nhóm -CO-NH- trong mạch nên thuộc nhóm tơ polyamide. Tơ nitron chỉ có mạch C-C và nhánh -CN.'
      },
      {
        id: 16,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Nhận biết',
        question: 'Tơ capron (nylon-6) có thể được điều chế trực tiếp bằng phản ứng trùng hợp chất nào sau đây?',
        options: [
          'Caprolactam',
          'Acrylonitrile',
          'Vinyl chloride',
          'Isoprene'
        ],
        answer: 0,
        equation: 'n Caprolactam (vòng 7 cạnh)  —(t°, xt)→  (-NH-[CH₂]₅-CO-)ₙ',
        explanation: 'Nylon-6 có 2 cách điều chế: trùng hợp mở vòng caprolactam hoặc trùng ngưng axit ε-aminocaproic.'
      },
      {
        id: 17,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Nhận biết',
        question: 'Sợi bông, len, tơ tằm đều thuộc loại:',
        options: [
          'Tơ thiên nhiên',
          'Tơ tổng hợp',
          'Tơ bán tổng hợp',
          'Tơ hóa học'
        ],
        answer: 0,
        equation: 'Bông (cellulose)  |  Len, Tơ tằm (protein)',
        explanation: 'Bông lấy từ quả bông, len từ lông cừu, tơ tằm từ kén tằm — tất cả đều có sẵn trong tự nhiên nên là tơ thiên nhiên.'
      },
      {
        id: 18,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Thông hiểu',
        question: 'Khi đốt cháy hoàn toàn một mẩu tơ, thấy có mùi khét như tóc cháy. Mẩu tơ đó có thể là:',
        options: [
          'Tơ tằm hoặc len lông cừu',
          'Sợi bông hoặc tơ visco',
          'Tơ nitron',
          'Tơ lapsan'
        ],
        answer: 0,
        equation: 'Protein  —(t°, O₂)→  CO₂ + H₂O + N₂ + mùi khét đặc trưng',
        explanation: 'Len và tơ tằm có bản chất là protein (chứa nitơ) nên khi đốt có mùi khét đặc trưng giống tóc cháy.'
      },
      {
        id: 19,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Vận dụng',
        question: 'Trong các loại tơ tổng hợp: tơ capron, tơ nylon-6,6, tơ nitron, tơ lapsan. Số loại tơ được điều chế bằng phản ứng TRÙNG NGƯNG (hoặc đồng trùng ngưng) là:',
        options: [
          '3 (capron, nylon-6,6, lapsan)',
          '2 (nylon-6,6, lapsan)',
          '1 (nylon-6,6)',
          '4 (tất cả)'
        ],
        answer: 0,
        equation: 'Capron (trùng ngưng ε-aminocaproic acid), Nylon-6,6 (đồng trùng ngưng), Lapsan (đồng trùng ngưng)',
        explanation: 'Tơ capron (từ axit ε-aminocaproic), nylon-6,6 và lapsan đều điều chế được bằng phản ứng trùng ngưng. Riêng tơ nitron chỉ điều chế bằng phản ứng trùng hợp.'
      },
      {
        id: 20,
        category: 'fiber',
        categoryLabel: 'Tơ sợi',
        difficulty: 'Thông hiểu',
        question: 'Bản chất hóa học của sợi bông và tơ visco lần lượt là:',
        options: [
          'Cellulose và dẫn xuất của cellulose',
          'Protein và cellulose',
          'Cellulose và polyamide',
          'Polyamide và polyester'
        ],
        answer: 0,
        equation: 'Sợi bông: (C₆H₁₀O₅)ₙ  |  Tơ visco: cellulose chế hóa với CS₂ và NaOH',
        explanation: 'Sợi bông là cellulose tự nhiên; tơ visco là cellulose đã qua chế hóa hóa học.'
      },

      // --- CAO SU (9 câu) ---
      {
        id: 21,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Nhận biết',
        question: 'Cao su buna-S được điều chế bằng phản ứng đồng trùng hợp giữa buta-1,3-diene với chất nào sau đây?',
        options: [
          'Styrene (C₆H₅-CH=CH₂)',
          'Lưu huỳnh (S)',
          'Acrylonitrile (CH₂=CH-CN)',
          'Isoprene'
        ],
        answer: 0,
        equation: 'nCH₂=CH-CH=CH₂ + mC₆H₅-CH=CH₂  —(xt, t°, p)→  Cao su buna-S',
        explanation: 'Chữ "S" trong buna-S là viết tắt của Styrene. Đồng trùng hợp buta-1,3-diene và styrene tạo cao su buna-S có tính đàn hồi cao.'
      },
      {
        id: 22,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Nhận biết',
        question: 'Cao su buna-N có tính chống dầu mỡ rất tốt, được điều chế bằng phản ứng đồng trùng hợp buta-1,3-diene với:',
        options: [
          'Acrylonitrile (CH₂=CH-CN)',
          'Sodium (Na)',
          'Styrene',
          'Chloroprene'
        ],
        answer: 0,
        equation: 'nCH₂=CH-CH=CH₂ + mCH₂=CH-CN  —(xt, t°, p)→  Cao su buna-N',
        explanation: 'Chữ "N" trong buna-N chỉ acrylonitrile (tạo tơ nitron). Đồng trùng hợp buta-1,3-diene với acrylonitrile cho cao su buna-N chống dầu tốt.'
      },
      {
        id: 23,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Thông hiểu',
        question: 'Bản chất của quá trình lưu hóa cao su (xử lý cao su với lưu huỳnh ở nhiệt độ cao) là:',
        options: [
          'Tạo cầu nối disulfide (-S-S-) khâu các mạch polymer thành mạng không gian',
          'Cắt ngắn mạch polymer để cao su mềm dẻo hơn',
          'Phản ứng trùng hợp thêm lưu huỳnh vào đầu mạch',
          'Thủy phân cao su thành các monomer nhỏ hơn'
        ],
        answer: 0,
        equation: 'Mạch cao su + S  —(t°)→  Mạng không gian với cầu nối -S-S-',
        explanation: 'Lưu hóa cao su là phản ứng tăng mạch cacbon nhờ cầu nối disulfide (-S-S-), biến cấu trúc mạch không nhánh thành mạng không gian bền chắc, đàn hồi hơn.'
      },
      {
        id: 24,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Nhận biết',
        question: 'Cao su thiên nhiên là polymer của monomer nào sau đây?',
        options: [
          'Isoprene (2-methylbuta-1,3-diene)',
          'Buta-1,3-diene',
          'Chloroprene',
          'Ethylene'
        ],
        answer: 0,
        equation: 'Mắt xích cao su thiên nhiên: (-CH₂-C(CH₃)=CH-CH₂-)ₙ (cấu hình cis)',
        explanation: 'Cao su thiên nhiên là polyisoprene, được khai thác từ mủ cây cao su.'
      },
      {
        id: 25,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Nhận biết',
        question: 'Loại cao su tổng hợp nào bền với dầu mỡ, hóa chất và khó cháy nên thường dùng làm ống dẫn dầu, đồ lặn, băng tải chịu nhiệt?',
        options: [
          'Cao su chloroprene',
          'Cao su buna',
          'Cao su isoprene',
          'Cao su thiên nhiên'
        ],
        answer: 0,
        equation: 'nCH₂=C(Cl)-CH=CH₂  —(xt, t°, p)→  (-CH₂-C(Cl)=CH-CH₂-)ₙ',
        explanation: 'Cao su chloroprene (trùng hợp 2-chlorobuta-1,3-diene) chứa nguyên tử Cl nên có đặc tính kháng dầu và khó cháy.'
      },
      {
        id: 26,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Thông hiểu',
        question: 'Trong phân tử cao su buna, mỗi mắt xích (-CH₂-CH=CH-CH₂-) còn chứa bao nhiêu liên kết đôi C=C?',
        options: [
          '1 liên kết đôi',
          '2 liên kết đôi',
          '0 liên kết đôi',
          '3 liên kết đôi'
        ],
        answer: 0,
        equation: 'nCH₂=CH-CH=CH₂  —(Na, t°, p)→  (-CH₂-CH=CH-CH₂-)ₙ',
        explanation: 'Monomer buta-1,3-diene có 2 liên kết đôi; khi trùng hợp 1,4 tạo thành mắt xích vẫn còn 1 liên kết đôi C=C ở giữa nên cao su vẫn làm mất màu nước brom.'
      },
      {
        id: 27,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Thông hiểu',
        question: 'So với cao su chưa lưu hóa, cao su lưu hóa có ưu điểm nào sau đây?',
        options: [
          'Độ đàn hồi cao hơn, chịu nhiệt tốt hơn, lâu mòn và khó tan trong dung môi hữu cơ',
          'Mềm hơn, dễ nóng chảy hơn và dễ tan trong xăng hơn',
          'Có cấu trúc mạch không phân nhánh nên dễ kéo sợi',
          'Dẫn điện và dẫn nhiệt tốt hơn kim loại'
        ],
        answer: 0,
        equation: 'Cao su thô (mạch không nhánh) + S → Cao su lưu hóa (mạng không gian)',
        explanation: 'Nhờ cấu trúc mạng không gian với cầu nối -S-S-, cao su lưu hóa bền cơ học, chịu nhiệt, đàn hồi tốt và không tan trong dung môi hữu cơ.'
      },
      {
        id: 28,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Nhận biết',
        question: 'Phản ứng trùng hợp buta-1,3-diene có mặt xúc tác kim loại Na ở nhiệt độ, áp suất thích hợp tạo ra sản phẩm là:',
        options: [
          'Cao su buna',
          'Cao su isoprene',
          'Cao su chloroprene',
          'Nhựa PE'
        ],
        answer: 0,
        equation: 'nCH₂=CH-CH=CH₂  —(Na, t°, p)→  (-CH₂-CH=CH-CH₂-)ₙ',
        explanation: 'Tên gọi "Buna" bắt nguồn từ chữ Bu (Butadiene) và Na (xúc tác Natri).'
      },
      {
        id: 29,
        category: 'rubber',
        categoryLabel: 'Cao su',
        difficulty: 'Vận dụng',
        question: 'Khi đun nóng cao su buna-S với dung dịch Br₂ dư trong CCl₄ thấy mất màu dung dịch Br₂. Nguyên nhân là do:',
        options: [
          'Trong mắt xích của buna-S còn liên kết đôi C=C của gốc butadiene',
          'Vòng benzen của styrene cộng hợp dễ dàng với Br₂',
          'Cao su bị thủy phân trong dung môi CCl₄',
          'Liên kết đơn C-C bị đứt gãy'
        ],
        answer: 0,
        equation: '(-CH₂-CH=CH-CH₂-CH₂-CH(C₆H₅)-)ₙ + nBr₂ → phản ứng cộng vào nối đôi C=C',
        explanation: 'Phần mắt xích từ buta-1,3-diene vẫn còn 1 liên kết đôi C=C nên tham gia phản ứng cộng làm mất màu dung dịch Br₂.'
      },

      // --- POLYMER THIÊN NHIÊN & VẬN DỤNG TỔNG HỢP (7 câu) ---
      {
        id: 30,
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        difficulty: 'Nhận biết',
        question: 'Tinh bột gồm hai thành phần là amylose và amylopectin. Phát biểu nào sau đây đúng về cấu trúc của chúng?',
        options: [
          'Amylose có mạch không phân nhánh, amylopectin có mạch phân nhánh',
          'Cả amylose và amylopectin đều có mạch không phân nhánh',
          'Amylose cấu tạo từ α-glucose, amylopectin cấu tạo từ β-glucose',
          'Cả hai đều có cấu trúc mạng không gian'
        ],
        answer: 0,
        equation: 'Tinh bột (C₆H₁₀O₅)ₙ = Amylose (mạch xoắn không nhánh) + Amylopectin (mạch phân nhánh)',
        explanation: 'Tinh bột được tạo thành từ các gốc α-glucose: amylose là mạch không phân nhánh, còn amylopectin chiếm tỉ lệ lớn hơn và có mạch phân nhánh.'
      },
      {
        id: 31,
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        difficulty: 'Thông hiểu',
        question: 'Điểm giống nhau giữa tinh bột và cellulose là:',
        options: [
          'Đều có công thức phân tử dạng (C₆H₁₀O₅)ₙ và thủy phân hoàn toàn đều thu được glucose',
          'Đều có cấu trúc mạch phân nhánh và tan trong nước nóng',
          'Đều được tạo thành từ các gốc β-glucose',
          'Đều dùng làm nguyên liệu trực tiếp để kéo tơ visco'
        ],
        answer: 0,
        equation: '(C₆H₁₀O₅)ₙ + nH₂O  —(H⁺, t°)→  nC₆H₁₂O₆ (glucose)',
        explanation: 'Tinh bột và cellulose đều là polysaccharide có công thức (C₆H₁₀O₅)ₙ (không phải đồng phân vì hệ số n khác nhau), thủy phân hoàn toàn đều cho glucose.'
      },
      {
        id: 32,
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        difficulty: 'Nhận biết',
        question: 'Protein là cơ sở tạo nên sự sống (cơ, da, tóc, enzyme...). Trong phân tử protein, các đơn vị cấu tạo liên kết với nhau bằng:',
        options: [
          'Liên kết peptide (-CO-NH-) giữa các gốc α-amino acid',
          'Liên kết glycoside giữa các gốc glucose',
          'Liên kết este (-COO-) giữa các axit và ancol',
          'Cầu nối disulfide (-S-S-) giữa các mạch hydrocarbon'
        ],
        answer: 0,
        equation: 'Chuỗi polypeptide: ...-NH-CH(R₁)-CO-NH-CH(R₂)-CO-...',
        explanation: 'Protein được tạo thành từ các chuỗi polypeptide kết hợp lại, trong đó các gốc α-amino acid nối với nhau bởi liên kết peptide (-CO-NH-).'
      },
      {
        id: 33,
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        difficulty: 'Thông hiểu',
        question: 'Cho các polymer sau: (1) cellulose, (2) nhựa bakelit (rezit), (3) cao su lưu hóa, (4) amylopectin. Những polymer có cấu trúc mạng không gian là:',
        options: [
          '(2) và (3)',
          '(1) và (4)',
          '(2), (3) và (4)',
          '(1), (2) và (3)'
        ],
        answer: 0,
        equation: 'Mạng không gian: Nhựa rezit (bakelit) và Cao su lưu hóa',
        explanation: 'Cellulose và amylose mạch không nhánh; amylopectin và glycogen mạch phân nhánh; chỉ có nhựa rezit và cao su lưu hóa có cấu trúc mạng không gian.'
      },
      {
        id: 34,
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        difficulty: 'Vận dụng',
        question: 'Cho dãy các polymer: PE, PVC, tơ nylon-6,6, tơ nitron, cao su buna, thủy tinh hữu cơ (PMMA). Số polymer được điều chế bằng phản ứng TRÙNG HỢP là:',
        options: [
          '5',
          '4',
          '6',
          '3'
        ],
        answer: 0,
        equation: 'Trùng hợp (5): PE, PVC, tơ nitron, cao su buna, PMMA.  |  Trùng ngưng (1): tơ nylon-6,6.',
        explanation: 'Chỉ có tơ nylon-6,6 được điều chế bằng phản ứng đồng trùng ngưng. 5 polymer còn lại (PE, PVC, tơ nitron, cao su buna, PMMA) đều từ phản ứng trùng hợp.'
      },
      {
        id: 35,
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        difficulty: 'Vận dụng',
        question: 'Cho các phát biểu sau:\n(a) Tơ visco và tơ cellulose acetate đều thuộc loại tơ tổng hợp.\n(b) Cao su lưu hóa có tính đàn hồi và chịu nhiệt tốt hơn cao su thường.\n(c) Trùng hợp acrylonitrile thu được tơ nitron dùng dệt vải may áo ấm.\n(d) Nhựa PE, PP, PVC đều là chất dẻo được điều chế bằng phản ứng trùng hợp.\nSố phát biểu ĐÚNG là:',
        options: [
          '3',
          '2',
          '4',
          '1'
        ],
        answer: 0,
        equation: '(a) Sai (là tơ bán tổng hợp / nhân tạo);  (b), (c), (d) Đúng.',
        explanation: 'Phát biểu (a) sai vì tơ visco và tơ cellulose acetate là tơ bán tổng hợp (nhân tạo), không phải tơ tổng hợp. Ba phát biểu (b), (c), (d) đều chính xác.'
      },
      {
        id: 36,
        category: 'natural',
        categoryLabel: 'Polymer thiên nhiên',
        difficulty: 'Vận dụng',
        question: 'Cho các phát biểu sau về polymer và vật liệu polymer:\n(1) Thủy tinh hữu cơ (PMMA) được dùng làm kính máy bay, kính chống đạn.\n(2) Tơ lapsan được điều chế từ ethylene glycol và adipic acid.\n(3) Khi nấu canh cua thấy xuất hiện gạch cua nổi lên là do sự đông tụ protein.\n(4) Cao su buna-N được điều chế bằng phản ứng đồng trùng hợp buta-1,3-diene với styrene.\nSố phát biểu ĐÚNG là:',
        options: [
          '2',
          '1',
          '3',
          '4'
        ],
        answer: 0,
        equation: '(1) Đúng;  (2) Sai (phải là terephthalic acid);  (3) Đúng;  (4) Sai (phải là acrylonitrile).',
        explanation: 'Có 2 phát biểu đúng là (1) và (3). Phát biểu (2) sai ở adipic acid (đúng là terephthalic acid); phát biểu (4) sai ở styrene (đúng là acrylonitrile).'
      }
    ];

    // =========================================================================
    // 3. DỮ LIỆU MINI-GAME GHÉP THẺ
    // =========================================================================
    const MATCH_PAIRS = {
      monomer: [
        { id: 'm1', left: 'Ethylene (CH₂=CH₂)', right: 'Polyethylene (PE)' },
        { id: 'm2', left: 'Vinyl chloride (CH₂=CH-Cl)', right: 'Poly(vinyl chloride) (PVC)' },
        { id: 'm3', left: 'Styrene (C₆H₅-CH=CH₂)', right: 'Polystyrene (PS)' },
        { id: 'm4', left: 'Methyl methacrylate', right: 'Thủy tinh hữu cơ (PMMA)' },
        { id: 'm5', left: 'Acrylonitrile (CH₂=CH-CN)', right: 'Tơ nitron (tơ olon)' },
        { id: 'm6', left: 'Buta-1,3-diene (xt Na)', right: 'Cao su buna' },
        { id: 'm7', left: 'Hexamethylenediamine + Adipic acid', right: 'Tơ nylon-6,6' },
        { id: 'm8', left: 'Ethylene glycol + Terephthalic acid', right: 'Tơ lapsan' },
        { id: 'm9', left: 'Phenol + Formaldehyde', right: 'Nhựa bakelit (PPF)' },
        { id: 'm10', left: 'Buta-1,3-diene + Styrene', right: 'Cao su buna-S' },
        { id: 'm11', left: 'Buta-1,3-diene + Acrylonitrile', right: 'Cao su buna-N' },
        { id: 'm12', left: 'Propylene (CH₂=CH-CH₃)', right: 'Polypropylene (PP)' }
      ],
      application: [
        { id: 'a1', left: 'Poly(vinyl chloride) (PVC)', right: 'Ống dẫn nước, áo mưa, vỏ dây điện' },
        { id: 'a2', left: 'PMMA (Thủy tinh hữu cơ)', right: 'Kính máy bay, kính chống đạn, bể cá' },
        { id: 'a3', left: 'Polystyrene (PS)', right: 'Hộp xốp đựng thức ăn, vỏ đồ điện tử' },
        { id: 'a4', left: 'Nhựa bakelit (PPF)', right: 'Tay cầm xoong chảo chịu nhiệt, ổ điện' },
        { id: 'a5', left: 'Polyethylene (PE)', right: 'Túi nilon, màng bọc thực phẩm' },
        { id: 'a6', left: 'Tơ nitron (tơ olon)', right: 'Dệt vải may quần áo ấm, sợi "len"' },
        { id: 'a7', left: 'Cao su buna-N', right: 'Gioăng cao su, ống dẫn xăng dầu' },
        { id: 'a8', left: 'Polypropylene (PP)', right: 'Bao bì, hộp thực phẩm, dây chão' },
        { id: 'a9', left: 'Cellulose', right: 'Thành phần chính của gỗ, bông, giấy' },
        { id: 'a10', left: 'Protein', right: 'Cấu tạo nên cơ, da, tóc, enzyme' }
      ],
      reaction: [
        { id: 'r1', left: 'Tơ visco, Tơ cellulose acetate', right: 'Tơ bán tổng hợp (nhân tạo)' },
        { id: 'r2', left: 'Bông, Len, Tơ tằm', right: 'Tơ thiên nhiên' },
        { id: 'r3', left: 'Nhựa bakelit (PPF)', right: 'Phản ứng trùng ngưng' },
        { id: 'r4', left: 'Cao su buna-S, Buna-N', right: 'Phản ứng đồng trùng hợp' },
        { id: 'r5', left: 'Cao su lưu hóa', right: 'Mạng không gian có cầu nối -S-S-' },
        { id: 'r6', left: 'Tinh bột', right: 'Gồm amylose và amylopectin' },
        { id: 'r7', left: 'Tơ nylon-6 (tơ capron)', right: 'Tơ polyamide (trùng hợp/trùng ngưng)' },
        { id: 'r8', left: 'Tơ lapsan', right: 'Tơ polyester (đồng trùng ngưng)' }
      ]
    };

    // =========================================================================
    // 4. QUẢN LÝ TRẠNG THÁI, LOCALSTORAGE, HAPTICS & CỬ CHỈ VUỐT MOBILE
    // =========================================================================
    const TAB_ORDER = ['handbook', 'quiz', 'match', 'stats'];
    let currentTab = 'handbook';
    let currentHandbookFilter = 'all';
    let expandedCardIds = new Set();

    // User Progress (Saved in localStorage)
    let userStats = {
      totalAnswered: 0,
      totalCorrect: 0,
      bestStreak: 0,
      wrongIds: []
    };

    // Quiz State
    let selectedTopic = 'all';
    let selectedCount = 10;
    let activeQuestions = [];
    let currentQuestionIdx = 0;
    let score = 0;
    let streak = 0;
    let maxStreak = 0;
    let answeredCurrent = false;
    let wrongQuestions = [];

    // Match Game State
    let matchSelectedLeft = null;
    let matchSelectedRight = null;
    let matchedCount = 0;
    let matchTotalPairs = 5;
    let matchAttempts = 0;
    let matchTimerInterval = null;
    let matchSeconds = 0;
    let isCheckingMatch = false;

    function triggerHaptic(pattern = 15) {
      if (typeof navigator !== 'undefined' && navigator.vibrate) {
        try {
          navigator.vibrate(pattern);
        } catch (e) {}
      }
    }

    function loadUserStats() {
      try {
        const raw = localStorage.getItem('polymaster_stats_v2');
        if (raw) {
          const parsed = JSON.parse(raw);
          userStats = {
            totalAnswered: parsed.totalAnswered || 0,
            totalCorrect: parsed.totalCorrect || 0,
            bestStreak: parsed.bestStreak || 0,
            wrongIds: Array.isArray(parsed.wrongIds) ? parsed.wrongIds : []
          };
        }
      } catch (e) {}
      updateStatsUI();
    }

    function saveUserStats() {
      try {
        localStorage.setItem('polymaster_stats_v2', JSON.stringify(userStats));
      } catch (e) {}
      updateStatsUI();
    }

    function updateStatsUI() {
      document.getElementById('header-best-streak').textContent = userStats.bestStreak;
      document.getElementById('stat-total-answered').textContent = userStats.totalAnswered;
      const rate = userStats.totalAnswered > 0
        ? Math.round((userStats.totalCorrect / userStats.totalAnswered) * 100)
        : 0;
      document.getElementById('stat-accuracy-rate').textContent = `${rate}%`;
      document.getElementById('stat-best-streak').textContent = `${userStats.bestStreak} 🔥`;
      document.getElementById('stat-saved-wrong').textContent = userStats.wrongIds.length;

      const badge = document.getElementById('nav-wrong-badge');
      if (userStats.wrongIds.length > 0) {
        badge.classList.remove('hidden');
      } else {
        badge.classList.add('hidden');
      }
    }

    // Theme Initialization
    function initTheme() {
      const saved = localStorage.getItem('polymaster_theme');
      if (saved === 'dark' || (!saved && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
        document.documentElement.classList.add('dark');
      } else {
        document.documentElement.classList.remove('dark');
      }
    }

    function toggleTheme() {
      triggerHaptic(12);
      const isDark = document.documentElement.classList.toggle('dark');
      localStorage.setItem('polymaster_theme', isDark ? 'dark' : 'light');
    }

    function switchTab(tab) {
      if (currentTab === tab) return;
      triggerHaptic(10);
      currentTab = tab;

      TAB_ORDER.forEach(t => {
        const view = document.getElementById(`view-${t}`);
        if (t === tab) {
          view.classList.remove('hidden');
        } else {
          view.classList.add('hidden');
        }
      });

      // Đồng bộ trạng thái active cho cả Desktop Top Nav và Mobile Bottom Nav
      document.querySelectorAll('.nav-tab-btn').forEach(btn => {
        const isTarget = btn.dataset.tab === tab;
        const isMobileBottom = btn.classList.contains('flex-col');
        if (isMobileBottom) {
          if (isTarget) {
            btn.className = 'nav-tab-btn min-h-[50px] rounded-xl flex flex-col items-center justify-center gap-0.5 text-indigo-600 dark:text-indigo-400 bg-indigo-50/90 dark:bg-indigo-950/70 font-bold transition-all active:scale-95 relative';
          } else {
            btn.className = 'nav-tab-btn min-h-[50px] rounded-xl flex flex-col items-center justify-center gap-0.5 text-slate-500 dark:text-slate-400 font-semibold transition-all active:scale-95 relative';
          }
        } else {
          if (isTarget) {
            btn.className = 'nav-tab-btn px-4 py-2 rounded-lg text-sm font-semibold transition-all flex items-center gap-1.5 bg-white dark:bg-slate-700 text-indigo-600 dark:text-indigo-300 shadow-sm';
          } else {
            btn.className = 'nav-tab-btn px-4 py-2 rounded-lg text-sm font-semibold transition-all flex items-center gap-1.5 text-slate-600 dark:text-slate-300 hover:text-slate-900 dark:hover:text-white';
          }
        }
      });

      window.scrollTo({ top: 0, behavior: 'smooth' });

      if (tab === 'match' && document.getElementById('match-col-left').children.length === 0) {
        initMatchGame();
      }
      if (tab === 'stats') {
        renderStatsView();
      }
    }

    // Cử chỉ vuốt ngang (Swipe trái/phải) để chuyển Tab nhanh trên điện thoại
    function initSwipeNavigation() {
      let touchStartX = 0;
      let touchStartY = 0;
      let ignoredSwipe = false;

      document.addEventListener('touchstart', (e) => {
        // Bỏ qua nếu người dùng đang vuốt trên vùng có thanh cuộn ngang (phương trình hóa học hoặc thanh lọc)
        if (e.target.closest('.overflow-x-auto')) {
          ignoredSwipe = true;
          return;
        }
        ignoredSwipe = false;
        touchStartX = e.changedTouches[0].screenX;
        touchStartY = e.changedTouches[0].screenY;
      }, { passive: true });

      document.addEventListener('touchend', (e) => {
        if (ignoredSwipe) return;
        // Không chuyển tab bằng vuốt khi đang làm bài trắc nghiệm để tránh thoát nhầm
        if (currentTab === 'quiz' && !document.getElementById('quiz-active').classList.contains('hidden')) {
          return;
        }
        const deltaX = e.changedTouches[0].screenX - touchStartX;
        const deltaY = e.changedTouches[0].screenY - touchStartY;

        if (Math.abs(deltaX) > 75 && Math.abs(deltaX) > Math.abs(deltaY) * 1.6) {
          const idx = TAB_ORDER.indexOf(currentTab);
          if (deltaX < 0 && idx < TAB_ORDER.length - 1) {
            switchTab(TAB_ORDER[idx + 1]);
          } else if (deltaX > 0 && idx > 0) {
            switchTab(TAB_ORDER[idx - 1]);
          }
        }
      }, { passive: true });
    }

    // =========================================================================
    // 5. LOGIC SỔ TAY PHƯƠNG TRÌNH (TỐI ƯU MOBILE)
    // =========================================================================
    function handleHandbookSearch() {
      const val = document.getElementById('handbook-search').value;
      const clearBtn = document.getElementById('handbook-clear-btn');
      if (val.length > 0) {
        clearBtn.classList.remove('hidden');
      } else {
        clearBtn.classList.add('hidden');
      }
      renderHandbook();
    }

    function clearHandbookSearch() {
      const input = document.getElementById('handbook-search');
      input.value = '';
      document.getElementById('handbook-clear-btn').classList.add('hidden');
      renderHandbook();
      input.focus();
    }

    function setHandbookFilter(cat) {
      triggerHaptic(10);
      currentHandbookFilter = cat;
      document.querySelectorAll('.hb-filter').forEach(btn => {
        if (btn.dataset.cat === cat) {
          btn.className = 'hb-filter snap-start shrink-0 min-h-[40px] px-3.5 py-2 rounded-xl text-xs sm:text-sm font-bold bg-indigo-600 text-white shadow-sm transition-all active:scale-95';
        } else {
          btn.className = 'hb-filter snap-start shrink-0 min-h-[40px] px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 dark:hover:bg-slate-700 transition-all active:scale-95';
        }
      });
      renderHandbook();
    }

    function toggleHandbookNote(id) {
      triggerHaptic(10);
      if (expandedCardIds.has(id)) {
        expandedCardIds.delete(id);
      } else {
        expandedCardIds.add(id);
      }
      const noteEl = document.getElementById(`hb-note-${id}`);
      const btnEl = document.getElementById(`hb-toggle-${id}`);
      if (noteEl && btnEl) {
        const isOpen = expandedCardIds.has(id);
        noteEl.classList.toggle('hidden', !isOpen);
        btnEl.innerHTML = isOpen
          ? '<span>Thu gọn mẹo thi</span> <span>▴</span>'
          : '<span>Xem mẹo thi nhanh</span> <span>▾</span>';
      }
    }

    function getCategoryBadgeStyle(cat) {
      switch (cat) {
        case 'plastic':
          return 'bg-blue-100 text-blue-700 dark:bg-blue-950 dark:text-blue-300 border-blue-200 dark:border-blue-800';
        case 'fiber':
          return 'bg-purple-100 text-purple-700 dark:bg-purple-950 dark:text-purple-300 border-purple-200 dark:border-purple-800';
        case 'rubber':
          return 'bg-amber-100 text-amber-800 dark:bg-amber-950 dark:text-amber-300 border-amber-200 dark:border-amber-800';
        default:
          return 'bg-emerald-100 text-emerald-700 dark:bg-emerald-950 dark:text-emerald-300 border-emerald-200 dark:border-emerald-800';
      }
    }

    function renderHandbook() {
      const query = document.getElementById('handbook-search').value.trim().toLowerCase();
      const grid = document.getElementById('handbook-grid');

      const filtered = HANDBOOK_DATA.filter(item => {
        const matchCat = currentHandbookFilter === 'all' || item.category === currentHandbookFilter;
        const searchable = `${item.name} ${item.monomer} ${item.reactionType} ${item.applications} ${item.note}`.toLowerCase();
        const matchText = !query || searchable.includes(query);
        return matchCat && matchText;
      });

      if (filtered.length === 0) {
        grid.innerHTML = `
          <div class="col-span-full text-center py-12 bg-white dark:bg-slate-900 rounded-2xl border border-slate-200 dark:border-slate-800">
            <div class="text-3xl mb-2">🔍</div>
            <p class="text-slate-500 dark:text-slate-400 font-medium text-sm">Không tìm thấy polymer phù hợp với từ khóa "${query}".</p>
          </div>
        `;
        return;
      }

      grid.innerHTML = filtered.map(item => {
        const isExpanded = expandedCardIds.has(item.id);
        return `
        <article class="bg-white dark:bg-slate-900 rounded-2xl p-4 sm:p-5 border border-slate-200 dark:border-slate-800 shadow-sm hover:border-indigo-300 dark:hover:border-indigo-700 transition-all flex flex-col justify-between min-w-0">
          <div class="min-w-0">
            <div class="flex items-start justify-between gap-2 mb-2.5">
              <h3 class="text-base sm:text-lg font-extrabold text-slate-900 dark:text-white leading-snug">${item.name}</h3>
              <span class="shrink-0 text-[11px] font-bold px-2.5 py-0.5 rounded-lg border ${getCategoryBadgeStyle(item.category)}">
                ${item.categoryLabel}
              </span>
            </div>

            <div class="space-y-1.5 text-xs sm:text-sm">
              <div class="leading-relaxed">
                <span class="font-semibold text-slate-500 dark:text-slate-400">Monomer:</span>
                <span class="chem-text font-semibold text-slate-800 dark:text-slate-200">${item.monomer}</span>
              </div>
              <div class="flex flex-wrap gap-1.5 items-center">
                <span class="font-semibold text-slate-500 dark:text-slate-400">Phản ứng:</span>
                <span class="px-2 py-0.5 rounded-md bg-indigo-50 dark:bg-indigo-950/80 text-indigo-700 dark:text-indigo-300 font-semibold text-xs">${item.reactionType}</span>
              </div>
            </div>

            <!-- Equation Box: Khung cuộn ngang mượt + tự co giãn chữ để phương trình dài không tràn màn hình -->
            <div class="my-3 p-3 rounded-xl bg-slate-50 dark:bg-slate-950 border border-slate-200/80 dark:border-slate-800 font-mono text-indigo-700 dark:text-indigo-300 overflow-x-auto whitespace-nowrap chem-eq">
              ${item.equation}
            </div>
          </div>

          <div class="pt-2.5 border-t border-slate-100 dark:border-slate-800/80 space-y-2 text-xs sm:text-sm">
            <div class="leading-relaxed">
              <span class="font-bold text-emerald-600 dark:text-emerald-400">✨ Ứng dụng:</span>
              <span class="text-slate-700 dark:text-slate-300">${item.applications}</span>
            </div>

            <div id="hb-note-${item.id}" class="${isExpanded ? '' : 'hidden'} p-2.5 rounded-xl bg-amber-50/70 dark:bg-amber-950/30 border border-amber-200/60 dark:border-amber-800/50 text-xs text-slate-700 dark:text-slate-300 leading-relaxed">
              💡 <strong>Mẹo nhớ thi:</strong> ${item.note}
            </div>

            <button id="hb-toggle-${item.id}" onclick="toggleHandbookNote('${item.id}')" class="w-full min-h-[38px] mt-1 rounded-xl bg-slate-50 dark:bg-slate-800/70 hover:bg-indigo-50 dark:hover:bg-indigo-950/40 text-indigo-600 dark:text-indigo-400 font-semibold text-xs flex items-center justify-center gap-1 transition-colors">
              ${isExpanded ? '<span>Thu gọn mẹo thi</span> <span>▴</span>' : '<span>Xem mẹo thi nhanh</span> <span>▾</span>'}
            </button>
          </div>
        </article>
      `}).join('');
    }

    // =========================================================================
    // 6. LOGIC TRẮC NGHIỆM CHUYÊN SÂU
    // =========================================================================
    function updateQuizBankCounts() {
      document.getElementById('total-bank-count').textContent = QUIZ_BANK.length;
      document.getElementById('count-all').textContent = `${QUIZ_BANK.length} câu`;
      ['plastic', 'fiber', 'rubber', 'natural'].forEach(cat => {
        const c = QUIZ_BANK.filter(q => q.category === cat).length;
        const el = document.getElementById(`count-${cat}`);
        if (el) el.textContent = `${c} câu`;
      });
    }

    function selectQuizTopic(topic) {
      triggerHaptic(10);
      selectedTopic = topic;
      document.querySelectorAll('.q-topic-btn').forEach(btn => {
        if (btn.dataset.topic === topic) {
          btn.classList.add('border-indigo-600', 'bg-indigo-50/70', 'dark:bg-indigo-950/50');
          btn.classList.remove('border-slate-200', 'dark:border-slate-800');
        } else {
          btn.classList.remove('border-indigo-600', 'bg-indigo-50/70', 'dark:bg-indigo-950/50');
          btn.classList.add('border-slate-200', 'dark:border-slate-800');
        }
      });
    }

    function selectQuizCount(count) {
      triggerHaptic(10);
      selectedCount = count;
      document.querySelectorAll('.q-count-btn').forEach(btn => {
        if (Number(btn.dataset.count) === count) {
          btn.className = 'q-count-btn min-h-[48px] py-2.5 rounded-xl border-2 border-indigo-600 bg-indigo-50/70 dark:bg-indigo-950/50 font-bold text-sm text-indigo-700 dark:text-indigo-300 transition-all active:scale-95';
        } else {
          btn.className = 'q-count-btn min-h-[48px] py-2.5 rounded-xl border-2 border-slate-200 dark:border-slate-800 font-semibold text-sm hover:border-indigo-400 transition-all active:scale-95';
        }
      });
    }

    function shuffleArray(arr) {
      const copy = [...arr];
      for (let i = copy.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [copy[i], copy[j]] = [copy[j], copy[i]];
      }
      return copy;
    }

    function startQuiz(customQuestions = null) {
      triggerHaptic(18);
      if (customQuestions) {
        activeQuestions = shuffleArray(customQuestions);
      } else {
        const pool = selectedTopic === 'all'
          ? QUIZ_BANK
          : QUIZ_BANK.filter(q => q.category === selectedTopic);
        activeQuestions = shuffleArray(pool).slice(0, selectedCount);
      }

      currentQuestionIdx = 0;
      score = 0;
      streak = 0;
      maxStreak = 0;
      wrongQuestions = [];

      document.getElementById('quiz-setup').classList.add('hidden');
      document.getElementById('quiz-result').classList.add('hidden');
      document.getElementById('quiz-active').classList.remove('hidden');

      renderCurrentQuestion();
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    function quitQuiz() {
      triggerHaptic(12);
      resetQuizToSetup();
    }

    function resetQuizToSetup() {
      document.getElementById('quiz-active').classList.add('hidden');
      document.getElementById('quiz-result').classList.add('hidden');
      document.getElementById('quiz-setup').classList.remove('hidden');
    }

    function renderCurrentQuestion() {
      answeredCurrent = false;
      const q = activeQuestions[currentQuestionIdx];
      const total = activeQuestions.length;

      // Update Top Bar
      document.getElementById('quiz-progress-text').textContent = `Câu ${currentQuestionIdx + 1} / ${total}`;
      document.getElementById('quiz-category-badge').textContent = q.categoryLabel;
      document.getElementById('quiz-mobile-cat').textContent = q.categoryLabel;
      document.getElementById('quiz-difficulty-tag').textContent = q.difficulty;
      document.getElementById('quiz-streak').textContent = streak;
      document.getElementById('quiz-score').textContent = score;
      document.getElementById('quiz-progress-bar').style.width = `${((currentQuestionIdx + 1) / total) * 100}%`;

      // Question text
      document.getElementById('quiz-question-text').innerHTML = q.question.replace(/\n/g, '<br/>');

      // Shuffle options while keeping track of the correct one
      const indexedOptions = q.options.map((text, idx) => ({
        text,
        isCorrect: idx === q.answer
      }));
      const shuffledOptions = shuffleArray(indexedOptions);
      const labels = ['A', 'B', 'C', 'D'];

      const optionsContainer = document.getElementById('quiz-options');
      optionsContainer.innerHTML = shuffledOptions.map((opt, i) => `
        <button type="button"
          onclick="handleAnswer(this, ${opt.isCorrect})"
          data-correct="${opt.isCorrect}"
          class="quiz-opt-btn w-full min-h-[54px] text-left p-3.5 sm:p-4 rounded-xl border-2 border-slate-200 dark:border-slate-800 hover:border-indigo-500 dark:hover:border-indigo-500 hover:bg-indigo-50/40 dark:hover:bg-indigo-950/30 transition-all active:scale-[0.99] flex items-center gap-3 group">
          <span class="opt-letter shrink-0 w-8 h-8 rounded-lg bg-slate-100 dark:bg-slate-800 group-hover:bg-indigo-600 group-hover:text-white font-bold text-xs sm:text-sm flex items-center justify-center transition-colors">
            ${labels[i]}
          </span>
          <span class="chem-text text-sm sm:text-base font-medium text-slate-800 dark:text-slate-200 leading-snug">${opt.text}</span>
        </button>
      `).join('');

      // Hide feedback & next btn
      document.getElementById('quiz-feedback').classList.add('hidden');
      document.getElementById('quiz-next-wrap').classList.add('hidden');
    }

    function handleAnswer(btn, isCorrect) {
      if (answeredCurrent) return;
      answeredCurrent = true;

      const q = activeQuestions[currentQuestionIdx];
      const allBtns = document.querySelectorAll('.quiz-opt-btn');

      allBtns.forEach(b => {
        b.disabled = true;
        b.classList.remove('hover:border-indigo-500', 'hover:bg-indigo-50/40', 'active:scale-[0.99]');
        const correctFlag = b.dataset.correct === 'true';
        const letterBadge = b.querySelector('.opt-letter');

        if (correctFlag) {
          b.classList.remove('border-slate-200', 'dark:border-slate-800');
          b.classList.add('border-emerald-500', 'bg-emerald-50', 'dark:bg-emerald-950/40');
          letterBadge.className = 'opt-letter shrink-0 w-8 h-8 rounded-lg bg-emerald-600 text-white font-bold text-xs sm:text-sm flex items-center justify-center';
        } else if (b === btn && !isCorrect) {
          b.classList.remove('border-slate-200', 'dark:border-slate-800');
          b.classList.add('border-rose-500', 'bg-rose-50', 'dark:bg-rose-950/40');
          letterBadge.className = 'opt-letter shrink-0 w-8 h-8 rounded-lg bg-rose-600 text-white font-bold text-xs sm:text-sm flex items-center justify-center';
        } else {
          b.classList.add('opacity-55');
        }
      });

      const feedbackBox = document.getElementById('quiz-feedback');
      const feedbackHeader = document.getElementById('feedback-header');

      // Cập nhật thống kê tổng & danh sách câu sai vào localStorage
      userStats.totalAnswered++;

      if (isCorrect) {
        triggerHaptic(25);
        score++;
        streak++;
        userStats.totalCorrect++;
        if (streak > maxStreak) maxStreak = streak;
        if (streak > userStats.bestStreak) userStats.bestStreak = streak;
        // Gỡ khỏi kho câu sai nếu làm đúng
        userStats.wrongIds = userStats.wrongIds.filter(id => id !== q.id);

        feedbackBox.className = 'mt-5 p-4 sm:p-5 rounded-2xl border border-emerald-200 dark:border-emerald-800/80 bg-emerald-50/70 dark:bg-emerald-950/30 transition-all animate-pop';
        feedbackHeader.innerHTML = `<span class="text-emerald-600 dark:text-emerald-400">✅ Chính xác! +1 điểm</span>`;
      } else {
        triggerHaptic([35, 50, 35]);
        streak = 0;
        wrongQuestions.push(q);
        if (!userStats.wrongIds.includes(q.id)) {
          userStats.wrongIds.push(q.id);
        }

        feedbackBox.className = 'mt-5 p-4 sm:p-5 rounded-2xl border border-rose-200 dark:border-rose-800/80 bg-rose-50/70 dark:bg-rose-950/30 transition-all animate-pop';
        feedbackHeader.innerHTML = `<span class="text-rose-600 dark:text-rose-400">❌ Chưa chính xác! Xem lời giải bên dưới:</span>`;
      }

      saveUserStats();

      document.getElementById('quiz-streak').textContent = streak;
      document.getElementById('quiz-score').textContent = score;
      document.getElementById('feedback-equation-box').innerHTML = `⚗️ ${q.equation}`;
      document.getElementById('feedback-explanation').innerHTML = q.explanation;

      feedbackBox.classList.remove('hidden');

      const nextWrap = document.getElementById('quiz-next-wrap');
      const nextBtn = document.getElementById('quiz-next-btn');
      nextWrap.classList.remove('hidden');

      if (currentQuestionIdx === activeQuestions.length - 1) {
        nextBtn.querySelector('span').textContent = 'Xem kết quả tổng kết';
      } else {
        nextBtn.querySelector('span').textContent = 'Câu tiếp theo';
      }

      // Cuộn nhẹ xuống để thấy rõ giải thích và nút tiếp theo trên màn hình nhỏ
      setTimeout(() => {
        feedbackBox.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
      }, 100);
    }

    function nextQuestion() {
      triggerHaptic(12);
      if (currentQuestionIdx < activeQuestions.length - 1) {
        currentQuestionIdx++;
        renderCurrentQuestion();
        window.scrollTo({ top: 0, behavior: 'smooth' });
      } else {
        showQuizResult();
      }
    }

    function showQuizResult() {
      document.getElementById('quiz-active').classList.add('hidden');
      document.getElementById('quiz-result').classList.remove('hidden');
      window.scrollTo({ top: 0, behavior: 'smooth' });

      const total = activeQuestions.length;
      const pct = Math.round((score / total) * 100);

      document.getElementById('result-score-text').textContent = `${score}/${total}`;
      document.getElementById('result-accuracy').textContent = `${pct}%`;
      document.getElementById('result-max-streak').textContent = `${maxStreak} 🔥`;

      let emoji = '🏆';
      let sub = 'Xuất sắc! Bạn đã sẵn sàng chinh phục mọi câu hỏi Polymer trong đề thi.';
      if (pct < 50) {
        emoji = '📚';
        sub = 'Đừng nản nhé! Hãy xem lại Sổ tay phương trình và làm lại các câu sai để ghi nhớ.';
      } else if (pct < 80) {
        emoji = '👏';
        sub = 'Khá tốt! Ôn lại một chút các câu nhầm lẫn là bạn sẽ đạt điểm tối đa.';
      }
      document.getElementById('result-emoji').textContent = emoji;
      document.getElementById('result-subtitle').textContent = sub;

      const retryBtn = document.getElementById('retry-wrong-btn');
      const wrongReviewSec = document.getElementById('wrong-review-section');
      const wrongReviewList = document.getElementById('wrong-review-list');

      if (wrongQuestions.length > 0) {
        retryBtn.classList.remove('hidden');
        document.getElementById('wrong-count-label').textContent = wrongQuestions.length;
        wrongReviewSec.classList.remove('hidden');
        wrongReviewList.innerHTML = wrongQuestions.map((wq, i) => `
          <div class="p-3.5 sm:p-4 rounded-xl bg-slate-50 dark:bg-slate-800/60 border border-slate-200 dark:border-slate-800 text-xs sm:text-sm">
            <div class="font-bold text-slate-900 dark:text-white mb-1">${i + 1}. ${wq.question.replace(/\n/g, ' ')}</div>
            <div class="text-emerald-600 dark:text-emerald-400 font-semibold mb-1.5">✓ Đáp án đúng: ${wq.options[wq.answer]}</div>
            <div class="p-2 rounded-lg bg-white dark:bg-slate-950 text-indigo-600 dark:text-indigo-300 font-mono overflow-x-auto whitespace-nowrap chem-eq">${wq.equation}</div>
          </div>
        `).join('');
      } else {
        retryBtn.classList.add('hidden');
        wrongReviewSec.classList.add('hidden');
      }
    }

    function retryWrongQuestions() {
      if (wrongQuestions.length > 0) {
        startQuiz([...wrongQuestions]);
      }
    }

    // =========================================================================
    // 7. LOGIC MINI-GAME GHÉP THẺ (TỐI ƯU MOBILE)
    // =========================================================================
    function initMatchGame() {
      clearInterval(matchTimerInterval);
      matchSelectedLeft = null;
      matchSelectedRight = null;
      matchedCount = 0;
      matchAttempts = 0;
      matchSeconds = 0;
      isCheckingMatch = false;

      document.getElementById('match-victory').classList.add('hidden');
      document.getElementById('match-attempts').textContent = '0';
      document.getElementById('match-timer').textContent = '00:00';

      const mode = document.getElementById('match-mode-select').value;
      const leftLabel = document.getElementById('match-left-label');
      const rightLabel = document.getElementById('match-right-label');
      if (mode === 'monomer') {
        leftLabel.textContent = 'Nhóm 1 • Monomer điều chế';
        rightLabel.textContent = 'Nhóm 2 • Polymer sản phẩm';
      } else if (mode === 'application') {
        leftLabel.textContent = 'Nhóm 1 • Tên Polymer';
        rightLabel.textContent = 'Nhóm 2 • Ứng dụng thực tế';
      } else {
        leftLabel.textContent = 'Nhóm 1 • Tên Polymer';
        rightLabel.textContent = 'Nhóm 2 • Phân loại / Phản ứng';
      }

      const pool = MATCH_PAIRS[mode] || MATCH_PAIRS.monomer;
      const selectedPairs = shuffleArray(pool).slice(0, 5);
      matchTotalPairs = selectedPairs.length;

      document.getElementById('match-progress').textContent = `0 / ${matchTotalPairs}`;

      const leftCards = shuffleArray(selectedPairs.map(p => ({ id: p.id, text: p.left })));
      const rightCards = shuffleArray(selectedPairs.map(p => ({ id: p.id, text: p.right })));

      const leftCol = document.getElementById('match-col-left');
      const rightCol = document.getElementById('match-col-right');

      leftCol.innerHTML = leftCards.map(c => `
        <button type="button" data-side="left" data-id="${c.id}" onclick="selectMatchCard(this)"
          class="match-card w-full min-h-[54px] p-3.5 rounded-xl bg-white dark:bg-slate-900 border-2 border-slate-200 dark:border-slate-800 hover:border-indigo-400 text-xs sm:text-sm font-bold text-slate-800 dark:text-slate-100 shadow-xs transition-all active:scale-[0.98] flex items-center justify-center text-center leading-snug chem-text">
          ${c.text}
        </button>
      `).join('');

      rightCol.innerHTML = rightCards.map(c => `
        <button type="button" data-side="right" data-id="${c.id}" onclick="selectMatchCard(this)"
          class="match-card w-full min-h-[54px] p-3.5 rounded-xl bg-white dark:bg-slate-900 border-2 border-slate-200 dark:border-slate-800 hover:border-cyan-400 text-xs sm:text-sm font-bold text-slate-800 dark:text-slate-100 shadow-xs transition-all active:scale-[0.98] flex items-center justify-center text-center leading-snug chem-text">
          ${c.text}
        </button>
      `).join('');

      matchTimerInterval = setInterval(() => {
        matchSeconds++;
        const mins = String(Math.floor(matchSeconds / 60)).padStart(2, '0');
        const secs = String(matchSeconds % 60).padStart(2, '0');
        document.getElementById('match-timer').textContent = `${mins}:${secs}`;
      }, 1000);
    }

    function selectMatchCard(card) {
      if (isCheckingMatch || card.disabled) return;
      triggerHaptic(12);
      const side = card.dataset.side;

      if (side === 'left') {
        if (matchSelectedLeft) {
          matchSelectedLeft.classList.remove('border-indigo-600', 'bg-indigo-50', 'dark:bg-indigo-950/60', 'ring-2', 'ring-indigo-500/30');
        }
        matchSelectedLeft = card;
        card.classList.add('border-indigo-600', 'bg-indigo-50', 'dark:bg-indigo-950/60', 'ring-2', 'ring-indigo-500/30');
      } else {
        if (matchSelectedRight) {
          matchSelectedRight.classList.remove('border-cyan-600', 'bg-cyan-50', 'dark:bg-cyan-950/60', 'ring-2', 'ring-cyan-500/30');
        }
        matchSelectedRight = card;
        card.classList.add('border-cyan-600', 'bg-cyan-50', 'dark:bg-cyan-950/60', 'ring-2', 'ring-cyan-500/30');
      }

      if (matchSelectedLeft && matchSelectedRight) {
        checkMatchPair();
      }
    }

    function checkMatchPair() {
      isCheckingMatch = true;
      matchAttempts++;
      document.getElementById('match-attempts').textContent = matchAttempts;

      const left = matchSelectedLeft;
      const right = matchSelectedRight;
      const isMatch = left.dataset.id === right.dataset.id;

      if (isMatch) {
        triggerHaptic(25);
        matchedCount++;
        document.getElementById('match-progress').textContent = `${matchedCount} / ${matchTotalPairs}`;

        [left, right].forEach(el => {
          el.disabled = true;
          el.className = 'match-card w-full min-h-[54px] p-3.5 rounded-xl bg-emerald-50 dark:bg-emerald-950/40 border-2 border-emerald-500 text-xs sm:text-sm font-bold text-emerald-700 dark:text-emerald-300 opacity-70 transition-all flex items-center justify-center text-center leading-snug chem-text';
        });

        matchSelectedLeft = null;
        matchSelectedRight = null;
        isCheckingMatch = false;

        if (matchedCount === matchTotalPairs) {
          clearInterval(matchTimerInterval);
          const timeStr = document.getElementById('match-timer').textContent;
          document.getElementById('match-victory-stats').textContent = `Thời gian hoàn thành: ${timeStr} • Số lượt ghép: ${matchAttempts}`;
          const vicEl = document.getElementById('match-victory');
          vicEl.classList.remove('hidden');
          vicEl.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
      } else {
        triggerHaptic([30, 40, 30]);
        [left, right].forEach(el => {
          el.classList.add('border-rose-500', 'bg-rose-50', 'dark:bg-rose-950/50', 'animate-shake');
        });

        setTimeout(() => {
          [left, right].forEach(el => {
            el.classList.remove(
              'border-indigo-600', 'bg-indigo-50', 'dark:bg-indigo-950/60',
              'border-cyan-600', 'bg-cyan-50', 'dark:bg-cyan-950/60',
              'border-rose-500', 'bg-rose-50', 'dark:bg-rose-950/50',
              'ring-2', 'ring-indigo-500/30', 'ring-cyan-500/30', 'animate-shake'
            );
          });
          matchSelectedLeft = null;
          matchSelectedRight = null;
          isCheckingMatch = false;
        }, 420);
      }
    }

    // =========================================================================
    // 8. LOGIC TAB THỐNG KÊ & KHO CÂU SAI
    // =========================================================================
    function renderStatsView() {
      updateStatsUI();
      const listEl = document.getElementById('saved-wrong-list');
      const practiceBtn = document.getElementById('practice-saved-wrong-btn');

      const savedWrongObjs = QUIZ_BANK.filter(q => userStats.wrongIds.includes(q.id));

      if (savedWrongObjs.length === 0) {
        practiceBtn.classList.add('hidden');
        listEl.innerHTML = `
          <div class="text-center py-8 px-4 rounded-2xl bg-slate-50 dark:bg-slate-800/50 border border-dashed border-slate-200 dark:border-slate-700">
            <div class="text-3xl mb-2">✨</div>
            <p class="text-sm font-semibold text-slate-700 dark:text-slate-200">Bạn chưa có câu sai nào cần ôn lại!</p>
            <p class="text-xs text-slate-500 dark:text-slate-400 mt-1">Hãy vào mục Trắc nghiệm để luyện tập thêm nhé.</p>
          </div>
        `;
        return;
      }

      practiceBtn.classList.remove('hidden');
      listEl.innerHTML = savedWrongObjs.map((q, idx) => `
        <div class="p-3.5 sm:p-4 rounded-xl bg-slate-50 dark:bg-slate-800/60 border border-slate-200 dark:border-slate-800 text-xs sm:text-sm">
          <div class="flex items-center justify-between gap-2 mb-1">
            <span class="text-[11px] font-bold px-2 py-0.5 rounded bg-rose-100 dark:bg-rose-950 text-rose-700 dark:text-rose-300">${q.categoryLabel}</span>
          </div>
          <div class="font-bold text-slate-900 dark:text-white mb-1.5 leading-snug">${idx + 1}. ${q.question.replace(/\n/g, ' ')}</div>
          <div class="text-emerald-600 dark:text-emerald-400 font-semibold mb-1.5">✓ Đáp án đúng: ${q.options[q.answer]}</div>
          <div class="p-2 rounded-lg bg-white dark:bg-slate-950 text-indigo-600 dark:text-indigo-300 font-mono overflow-x-auto whitespace-nowrap chem-eq">${q.equation}</div>
        </div>
      `).join('');
    }

    function practiceSavedWrong() {
      const savedWrongObjs = QUIZ_BANK.filter(q => userStats.wrongIds.includes(q.id));
      if (savedWrongObjs.length > 0) {
        switchTab('quiz');
        startQuiz(savedWrongObjs);
      }
    }

    function confirmResetStats() {
      triggerHaptic(15);
      document.getElementById('reset-modal').classList.remove('hidden');
    }

    function closeResetModal() {
      document.getElementById('reset-modal').classList.add('hidden');
    }

    function executeResetStats() {
      userStats = { totalAnswered: 0, totalCorrect: 0, bestStreak: 0, wrongIds: [] };
      saveUserStats();
      closeResetModal();
      renderStatsView();
    }

    // =========================================================================
    // KHỞI CHẠY ỨNG DỤNG
    // =========================================================================
    window.addEventListener('DOMContentLoaded', () => {
      initTheme();
      loadUserStats();
      renderHandbook();
      updateQuizBankCounts();
      initSwipeNavigation();
    });
  </script>
</body>
</html>
