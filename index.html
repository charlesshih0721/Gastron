<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
  <title>美味快點 FoodOrder｜外送與自取點餐平台</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Noto+Sans+TC:wght@400;500;700;900&display=swap" rel="stylesheet">
  <script>
    // 提前定義圖片錯誤兜底函式，避免 HTML 解析期間找不到函式
    const FALLBACK_IMG = "https://placehold.co/800x450/f5f5f5/737373?text=FoodOrder";
    function handleImgError(el) {
      if (!el || el.dataset.fallbackApplied) return;
      el.dataset.fallbackApplied = "1";
      el.onerror = null;
      el.src = FALLBACK_IMG;
    }
  </script>
  <style>
    body {
      font-family: 'Inter', 'Noto Sans TC', -apple-system, BlinkMacSystemFont, sans-serif;
      background-color: #ffffff;
      color: #111111;
    }
    .no-scrollbar::-webkit-scrollbar { display: none; }
    .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    .safe-bottom {
      padding-bottom: max(1rem, env(safe-area-inset-bottom));
    }
    @keyframes fadeSlideUp {
      from { opacity: 0; transform: translateY(8px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .animate-fade-up { animation: fadeSlideUp 0.25s ease-out; }
  </style>
</head>
<body class="min-h-screen flex flex-col antialiased selection:bg-[#06C167] selection:text-white">

  <!-- ==================== 頂部導覽列 ==================== -->
  <header class="bg-white/95 backdrop-blur-sm border-b border-neutral-200 sticky top-0 z-30">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 h-16 flex items-center justify-between gap-3">
      <!-- 左側：品牌 Logo + 外送/自取分流 + 地址顯示 -->
      <div class="flex items-center gap-3 sm:gap-5 min-w-0">
        <button type="button" onclick="switchTab('home')" class="flex items-center gap-2 shrink-0 text-left group cursor-pointer">
          <div class="w-9 h-9 rounded-xl bg-neutral-950 flex items-center justify-center text-[#06C167] font-black text-lg tracking-tighter group-hover:scale-105 transition">
            F
          </div>
          <div class="hidden sm:block leading-none">
            <span class="font-extrabold text-lg tracking-tight text-neutral-950">Food<span class="text-[#06C167]">Order</span></span>
            <span class="block text-[10px] font-medium text-neutral-500 mt-0.5">美味快點外送平台</span>
          </div>
        </button>

        <!-- 外送 / 自取切換 -->
        <div class="flex items-center bg-neutral-100 rounded-full p-1 text-xs font-semibold shrink-0" role="group" aria-label="取餐方式切換">
          <button id="mode-delivery" type="button" onclick="setDeliveryMode('delivery')" class="px-3.5 py-1.5 rounded-full transition cursor-pointer">外送</button>
          <button id="mode-pickup" type="button" onclick="setDeliveryMode('pickup')" class="px-3.5 py-1.5 rounded-full transition cursor-pointer">來店自取</button>
        </div>

        <!-- 配送地址顯示（點擊可於 Google 地圖修改外送地址） -->
        <button type="button" onclick="openAddressModal('edit')" class="hidden xl:flex items-center gap-1.5 text-xs font-medium text-neutral-700 bg-neutral-100 hover:bg-neutral-200/70 px-3.5 py-2 rounded-full transition cursor-pointer">
          <svg class="w-4 h-4 text-[#059652] shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 21s-6-5.686-6-10a6 6 0 1112 0c0 4.314-6 10-6 10z"/>
            <circle cx="12" cy="11" r="2.5"/>
          </svg>
          <span id="header-location-label" class="truncate max-w-[190px]">台中市霧峰區中正路800號 • 立即送達</span>
          <svg class="w-3.5 h-3.5 text-neutral-400 shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7"/>
          </svg>
        </button>
      </div>

      <!-- 中央：即時搜尋列（桌面版） -->
      <div class="hidden md:flex flex-1 max-w-md relative">
        <svg class="w-4 h-4 text-neutral-400 absolute left-3.5 top-1/2 -translate-y-1/2 pointer-events-none" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <circle cx="11" cy="11" r="7"/><path stroke-linecap="round" d="M20 20l-3.5-3.5"/>
        </svg>
        <input id="search-input-desktop" type="text" oninput="handleSearchInput(this.value)" placeholder="搜尋餐廳、料理、餐點或關鍵字（如起司、珍珠）"
          class="w-full pl-10 pr-4 py-2 bg-neutral-100 hover:bg-neutral-200/70 focus:bg-white focus:ring-2 focus:ring-neutral-900 rounded-full text-sm transition outline-none placeholder:text-neutral-500" />
      </div>

      <!-- 右側：會員狀態 + 帳號登入 + 購物車 -->
      <div class="flex items-center gap-2 shrink-0">
        <button id="vip-badge-btn" type="button" onclick="openVipModal()" class="hidden sm:inline-flex items-center gap-1.5 px-3.5 py-2 rounded-full text-xs font-bold transition cursor-pointer"></button>

        <button id="user-account-btn" type="button" onclick="openLoginModal()" class="inline-flex items-center gap-2 px-3.5 py-2 rounded-full bg-neutral-100 hover:bg-neutral-200 text-xs font-semibold text-neutral-900 transition cursor-pointer">
          <span id="header-user-avatar" class="w-5 h-5 rounded-full bg-neutral-300 text-neutral-700 flex items-center justify-center text-[10px] font-bold">
            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2"/><circle cx="12" cy="7" r="4"/>
            </svg>
          </span>
          <span id="user-name-label" class="max-w-[84px] truncate">登入</span>
        </button>

        <button type="button" onclick="switchTab('cart')" aria-label="前往購物車" class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-neutral-950 hover:bg-neutral-800 text-white text-xs font-semibold transition cursor-pointer shadow-sm">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-1.5 6h13M10 21a1 1 0 100-2 1 1 0 000 2zm8 0a1 1 0 100-2 1 1 0 000 2z"/>
          </svg>
          <span class="hidden sm:inline">購物車</span>
          <span id="cart-count-badge" class="bg-[#06C167] text-neutral-950 rounded-full min-w-[20px] h-5 px-1.5 inline-flex items-center justify-center text-[11px] font-extrabold">0</span>
        </button>
      </div>
    </div>

    <!-- 手機版搜尋列與地址快捷列 -->
    <div class="md:hidden px-4 pb-2.5 space-y-2">
      <div class="relative">
        <svg class="w-4 h-4 text-neutral-400 absolute left-3.5 top-1/2 -translate-y-1/2 pointer-events-none" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <circle cx="11" cy="11" r="7"/><path stroke-linecap="round" d="M20 20l-3.5-3.5"/>
        </svg>
        <input id="search-input-mobile" type="text" oninput="handleSearchInput(this.value)" placeholder="搜尋餐廳、料理或餐點關鍵字..."
          class="w-full pl-10 pr-4 py-2 bg-neutral-100 focus:bg-white focus:ring-2 focus:ring-neutral-900 rounded-full text-sm outline-none" />
      </div>
      <div class="flex items-center justify-between gap-2">
        <button type="button" onclick="openAddressModal('edit')" class="flex-1 flex items-center gap-1.5 text-xs font-medium text-neutral-700 bg-neutral-100 px-3 py-1.5 rounded-full truncate">
          <svg class="w-3.5 h-3.5 text-[#059652] shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 21s-6-5.686-6-10a6 6 0 1112 0c0 4.314-6 10-6 10z"/><circle cx="12" cy="11" r="2.5"/>
          </svg>
          <span id="mobile-location-label" class="truncate">台中市霧峰區中正路800號</span>
        </button>
        <button id="vip-badge-mobile" type="button" onclick="openVipModal()" class="px-3 py-1.5 rounded-full text-xs font-bold shrink-0"></button>
      </div>
    </div>

    <!-- 主導覽分頁 -->
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 flex gap-6 text-sm font-semibold border-t border-neutral-100 overflow-x-auto no-scrollbar">
      <button id="tab-home" type="button" onclick="switchTab('home')" class="py-3 border-b-2 whitespace-nowrap transition cursor-pointer">探索餐廳</button>
      <button id="tab-favorites" type="button" onclick="switchTab('favorites')" class="py-3 border-b-2 whitespace-nowrap transition cursor-pointer">口袋名單</button>
      <button id="tab-orders" type="button" onclick="switchTab('orders')" class="py-3 border-b-2 whitespace-nowrap transition cursor-pointer">歷史訂單</button>
      <button id="tab-cart" type="button" onclick="switchTab('cart')" class="py-3 border-b-2 whitespace-nowrap transition cursor-pointer">結帳購物車</button>
    </nav>
  </header>

  <!-- ==================== 主內容區塊 ==================== -->
  <main class="max-w-7xl w-full mx-auto px-4 sm:px-6 py-6 flex-1">

    <!-- ==================== 分頁 1：首頁探索與智慧推薦 ==================== -->
    <section id="view-home" class="space-y-8 animate-fade-up">

      <!-- FoodOrder One 會員推廣深色橫幅 -->
      <div class="relative overflow-hidden rounded-2xl bg-neutral-950 text-white p-6 sm:p-8 flex flex-col md:flex-row items-start md:items-center justify-between gap-6">
        <div class="relative z-10 max-w-xl space-y-2">
          <div class="inline-flex items-center gap-2 text-xs font-bold uppercase tracking-wider text-[#06C167]">
            <span class="w-2 h-2 rounded-full bg-[#06C167]"></span>
            FoodOrder One 尊榮會員
          </div>
          <h1 class="text-2xl sm:text-3xl font-extrabold tracking-tight leading-tight">
            無限次 $0 外送費與免服務費，再享專屬折扣碼
          </h1>
          <p class="text-sm text-neutral-300">
            升級付費會員立即省下每筆 $39 外送費與 $15 平台服務費，結帳輸入 <span class="font-mono font-bold text-white">PRO85</span> 享 85 折或 <span class="font-mono font-bold text-white">VIP50</span> 現折 $50。
          </p>
        </div>
        <div class="relative z-10 flex items-center gap-3 shrink-0">
          <button id="hero-vip-btn" type="button" onclick="openVipModal()" class="px-5 py-3 rounded-full bg-[#06C167] hover:bg-[#05a858] text-neutral-950 font-bold text-sm transition cursor-pointer shadow-md">
            立即體驗 FoodOrder One
          </button>
        </div>
        <div class="absolute -right-16 -top-16 w-64 h-64 rounded-full bg-[#06C167]/15 blur-3xl pointer-events-none"></div>
      </div>

      <!-- 餐廳分類快速篩選 -->
      <div class="flex items-center justify-between gap-4 border-b border-neutral-100 pb-4">
        <div id="restaurant-category-tabs" class="flex items-center gap-2 overflow-x-auto no-scrollbar pb-1"></div>
      </div>

      <!-- 為您推薦：橫排 4 卡可左右滑動輪播（小圖示精巧版） -->
      <div class="space-y-3">
        <div class="flex flex-wrap items-end justify-between gap-3">
          <div class="space-y-1">
            <div class="flex items-center gap-2">
              <h2 class="text-xl font-extrabold tracking-tight text-neutral-950">為您推薦</h2>
              <span class="text-[11px] font-bold px-2.5 py-0.5 rounded-full bg-emerald-50 text-[#059652] border border-emerald-200">AI 口味分析</span>
            </div>
            <p id="rec-reason" class="text-xs text-neutral-500"></p>
          </div>
          <div class="flex items-center gap-3">
            <div id="taste-stats-pills" class="hidden sm:flex flex-wrap gap-1.5 text-xs"></div>
            <div class="flex items-center gap-1.5 shrink-0">
              <button type="button" onclick="scrollRecommendations(-1)" aria-label="向左滑動推薦餐廳"
                class="w-8 h-8 rounded-full border border-neutral-200 bg-white hover:bg-neutral-100 flex items-center justify-center text-neutral-700 transition cursor-pointer shadow-sm">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M15 19l-7-7 7-7"/></svg>
              </button>
              <button type="button" onclick="scrollRecommendations(1)" aria-label="向右滑動推薦餐廳"
                class="w-8 h-8 rounded-full border border-neutral-200 bg-white hover:bg-neutral-100 flex items-center justify-center text-neutral-700 transition cursor-pointer shadow-sm">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7"/></svg>
              </button>
            </div>
          </div>
        </div>
        <!-- 橫向滑動容器：桌面版一次顯示 4 家 -->
        <div id="recommended-carousel" class="flex gap-4 overflow-x-auto no-scrollbar snap-x snap-mandatory pb-2 scroll-smooth"></div>
      </div>

      <!-- 附近熱門餐廳（標準 3 欄大圖卡片） -->
      <div class="space-y-4 pt-2">
        <div class="flex items-center justify-between">
          <h2 class="text-xl font-extrabold tracking-tight text-neutral-950">附近熱門餐廳</h2>
          <span id="restaurants-count-label" class="text-xs font-medium text-neutral-500"></span>
        </div>
        <div id="restaurants-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6"></div>
      </div>
    </section>

    <!-- ==================== 分頁 2：我的口袋名單 ==================== -->
    <section id="view-favorites" class="hidden space-y-5 animate-fade-up">
      <div class="flex items-center justify-between border-b border-neutral-100 pb-4">
        <div>
          <h2 class="text-2xl font-extrabold tracking-tight">我的口袋名單</h2>
          <p class="text-sm text-neutral-500 mt-0.5">您收藏的精選愛店，隨時快速回購</p>
        </div>
      </div>
      <div id="favorites-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6"></div>
    </section>

    <!-- ==================== 分頁 3：歷史訂單與即時狀態追蹤 ==================== -->
    <section id="view-orders" class="hidden space-y-5 animate-fade-up">
      <div class="flex flex-wrap items-center justify-between gap-3 border-b border-neutral-100 pb-4">
        <div>
          <h2 class="text-2xl font-extrabold tracking-tight">歷史訂單與即時追蹤</h2>
          <p class="text-sm text-neutral-500 mt-0.5">追蹤餐點即時進度，或一鍵「再次點購」過往美味</p>
        </div>
        <label class="inline-flex items-center gap-2 text-xs font-semibold text-neutral-700 bg-neutral-100 px-3.5 py-2 rounded-full cursor-pointer select-none">
          <input id="auto-advance-toggle" type="checkbox" onchange="toggleAutoAdvance(this.checked)" class="accent-[#06C167] w-4 h-4 rounded" />
          <span>自動模擬推進訂單進度（每 8 秒）</span>
        </label>
      </div>
      <div id="orders-list" class="space-y-4"></div>
    </section>

    <!-- ==================== 分頁 4：購物車與線上結帳 ==================== -->
    <section id="view-cart" class="hidden animate-fade-up">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
        <!-- 左側購物車清單（按餐廳分組） -->
        <div class="lg:col-span-7 space-y-4">
          <div class="flex items-center justify-between border-b border-neutral-200 pb-3">
            <h2 class="text-2xl font-extrabold tracking-tight">購物車明細</h2>
            <button id="clear-cart-btn" type="button" onclick="clearCart()" class="text-xs font-semibold text-neutral-500 hover:text-red-600 transition cursor-pointer">清空購物車</button>
          </div>
          <div id="cross-store-notice" class="hidden p-3.5 rounded-xl bg-amber-50 border border-amber-200 text-xs text-amber-900 font-medium"></div>
          <div id="cart-items-list" class="space-y-4"></div>
        </div>

        <!-- 右側結帳摘要卡片 -->
        <div class="lg:col-span-5 bg-neutral-50 border border-neutral-200 rounded-2xl p-6 space-y-5 sticky top-28">
          <h3 class="text-lg font-extrabold tracking-tight">結帳摘要</h3>

          <!-- 會員權益提示卡 -->
          <div id="vip-promo-banner" class="p-3.5 rounded-xl text-xs leading-relaxed"></div>

          <!-- 優惠碼輸入區 -->
          <div class="space-y-1.5">
            <label for="promo-input" class="text-xs font-bold text-neutral-700 block">專屬折扣碼（付費會員適用：PRO85 / VIP50）</label>
            <div class="flex gap-2">
              <input id="promo-input" type="text" oninput="handlePromoInput(this.value)" placeholder="輸入優惠碼"
                class="flex-1 px-3.5 py-2 bg-white border border-neutral-300 rounded-xl text-sm uppercase focus:outline-none focus:border-neutral-900 disabled:bg-neutral-100 disabled:text-neutral-400" />
              <button id="apply-promo-btn" type="button" onclick="applyPromo()"
                class="px-4 py-2 bg-neutral-900 hover:bg-neutral-800 disabled:bg-neutral-300 text-white rounded-xl text-xs font-semibold transition cursor-pointer">
                套用
              </button>
            </div>
            <p id="promo-msg" class="text-xs min-h-[16px]"></p>
          </div>

          <!-- 付款方式選擇 -->
          <div class="space-y-2.5 border-t border-neutral-200 pt-4">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold text-neutral-800">付款方式</span>
              <span id="selected-payment-badge" class="text-[11px] font-semibold text-[#059652]"></span>
            </div>
            <div class="grid grid-cols-1 gap-2 text-xs">
              <!-- 貨到付款 -->
              <label class="flex items-center justify-between p-3 bg-white border rounded-xl cursor-pointer hover:border-neutral-400 transition">
                <div class="flex items-center gap-2.5">
                  <input type="radio" name="payment-method" value="cash" onchange="selectPaymentMethod('cash')" class="accent-neutral-950" />
                  <div>
                    <p id="cash-payment-label" class="font-bold text-neutral-900">貨到付款（現金）</p>
                    <p class="text-[11px] text-neutral-500">餐點送達時以現金支付</p>
                  </div>
                </div>
                <span class="px-2 py-0.5 rounded bg-neutral-100 text-neutral-600 font-semibold text-[10px]">現金</span>
              </label>

              <!-- 信用卡 / 金融卡 -->
              <div class="bg-white border rounded-xl overflow-hidden transition">
                <label class="flex items-center justify-between p-3 cursor-pointer hover:bg-neutral-50/70">
                  <div class="flex items-center gap-2.5">
                    <input type="radio" name="payment-method" value="card" onchange="selectPaymentMethod('card')" class="accent-neutral-950" />
                    <div>
                      <p class="font-bold text-neutral-900">信用卡 / 金融卡</p>
                      <p class="text-[11px] text-neutral-500">支援 Visa、Mastercard、JCB</p>
                    </div>
                  </div>
                  <div class="flex items-center gap-1 text-[10px] font-extrabold">
                    <span class="px-1.5 py-0.5 rounded bg-blue-50 text-blue-700">VISA</span>
                    <span class="px-1.5 py-0.5 rounded bg-orange-50 text-orange-700">MC</span>
                    <span class="px-1.5 py-0.5 rounded bg-emerald-50 text-emerald-700">JCB</span>
                  </div>
                </label>

                <!-- 展開的卡片選擇與新卡表單 -->
                <div id="card-options-panel" class="hidden border-t border-neutral-100 p-3 bg-neutral-50/70 space-y-2.5">
                  <div id="saved-cards-list" class="space-y-1.5"></div>
                  <button type="button" onclick="toggleNewCardForm()" class="text-[11px] font-bold text-[#059652] hover:underline cursor-pointer">
                    + 輸入新卡號
                  </button>
                  <div id="new-card-form" class="hidden space-y-2 pt-1">
                    <div class="relative">
                      <input id="new-card-number" type="text" maxlength="19" oninput="formatNewCardNumber(this)" placeholder="卡號（例如 4242 4242 4242 4242）"
                        class="w-full px-3 py-2 bg-white border border-neutral-300 rounded-lg text-xs font-mono focus:outline-none focus:border-neutral-900" />
                      <span id="new-card-brand-tag" class="absolute right-2.5 top-1/2 -translate-y-1/2 text-[10px] font-extrabold text-neutral-400"></span>
                    </div>
                    <div class="grid grid-cols-2 gap-2">
                      <input id="new-card-expiry" type="text" maxlength="5" oninput="formatCardExpiry(this)" placeholder="有效期限 MM/YY"
                        class="px-3 py-2 bg-white border border-neutral-300 rounded-lg text-xs font-mono focus:outline-none focus:border-neutral-900" />
                      <input id="new-card-cvv" type="password" maxlength="4" placeholder="安全碼 CVV"
                        class="px-3 py-2 bg-white border border-neutral-300 rounded-lg text-xs font-mono focus:outline-none focus:border-neutral-900" />
                    </div>
                  </div>
                </div>
              </div>

              <!-- 行動支付 -->
              <div class="grid grid-cols-3 gap-2">
                <label class="flex flex-col items-center justify-center p-2.5 bg-white border rounded-xl cursor-pointer hover:border-neutral-400 transition text-center gap-1">
                  <input type="radio" name="payment-method" value="linepay" onchange="selectPaymentMethod('linepay')" class="accent-[#06C167]" />
                  <span class="font-extrabold text-[#06C167]">LINE Pay</span>
                </label>
                <label class="flex flex-col items-center justify-center p-2.5 bg-white border rounded-xl cursor-pointer hover:border-neutral-400 transition text-center gap-1">
                  <input type="radio" name="payment-method" value="applepay" onchange="selectPaymentMethod('applepay')" class="accent-neutral-950" />
                  <span class="font-extrabold text-neutral-950">Apple Pay</span>
                </label>
                <label class="flex flex-col items-center justify-center p-2.5 bg-white border rounded-xl cursor-pointer hover:border-neutral-400 transition text-center gap-1">
                  <input type="radio" name="payment-method" value="jkopay" onchange="selectPaymentMethod('jkopay')" class="accent-red-600" />
                  <span class="font-extrabold text-red-600">街口支付</span>
                </label>
              </div>
            </div>
          </div>

          <!-- 電子發票與載具設定 -->
          <div class="space-y-2.5 border-t border-neutral-200 pt-4">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold text-neutral-800">電子發票 / 載具</span>
              <span id="invoice-bound-hint" class="text-[11px] font-semibold text-[#059652]"></span>
            </div>
            <div class="grid grid-cols-2 gap-1.5 text-xs">
              <button type="button" id="inv-btn-carrier" onclick="selectInvoiceType('carrier')" class="py-2 px-2.5 rounded-lg border font-semibold transition cursor-pointer">手機條碼載具</button>
              <button type="button" id="inv-btn-member" onclick="selectInvoiceType('member')" class="py-2 px-2.5 rounded-lg border font-semibold transition cursor-pointer">會員雲端發票</button>
              <button type="button" id="inv-btn-donate" onclick="selectInvoiceType('donate')" class="py-2 px-2.5 rounded-lg border font-semibold transition cursor-pointer">愛心捐贈碼</button>
              <button type="button" id="inv-btn-company" onclick="selectInvoiceType('company')" class="py-2 px-2.5 rounded-lg border font-semibold transition cursor-pointer">公司統一編號</button>
            </div>

            <!-- 載具輸入面板 -->
            <div id="inv-panel-carrier" class="hidden space-y-1.5">
              <div class="flex gap-2">
                <input id="checkout-carrier-input" type="text" maxlength="8" oninput="handleCheckoutCarrierInput(this)" placeholder="輸入手機條碼（如 /AB12345）"
                  class="flex-1 px-3 py-2 bg-white border border-neutral-300 rounded-lg text-xs font-mono uppercase focus:outline-none focus:border-neutral-900" />
                <button type="button" onclick="quickBindCarrierFromCheckout()" class="px-3 py-2 bg-neutral-900 hover:bg-neutral-800 text-white rounded-lg text-[11px] font-semibold cursor-pointer shrink-0">
                  綁定帳號
                </button>
              </div>
              <p class="text-[11px] text-neutral-500">格式為「/」開頭加上 7 碼英數字或符號（共 8 碼）</p>
            </div>

            <!-- 捐贈碼面板 -->
            <div id="inv-panel-donate" class="hidden space-y-1.5">
              <input id="checkout-donate-input" type="text" maxlength="7" oninput="invoiceDonateCode = this.value.trim()" placeholder="輸入 3~7 碼愛心捐贈碼"
                class="w-full px-3 py-2 bg-white border border-neutral-300 rounded-lg text-xs font-mono focus:outline-none focus:border-neutral-900" />
              <div class="flex gap-1.5 text-[11px]">
                <button type="button" onclick="setDonatePreset('919')" class="px-2 py-1 rounded bg-neutral-200/70 hover:bg-neutral-200 font-medium cursor-pointer">919 創世基金會</button>
                <button type="button" onclick="setDonatePreset('168001')" class="px-2 py-1 rounded bg-neutral-200/70 hover:bg-neutral-200 font-medium cursor-pointer">168001 導盲犬協會</button>
              </div>
            </div>

            <!-- 統編面板 -->
            <div id="inv-panel-company" class="hidden space-y-1">
              <input id="checkout-taxid-input" type="text" maxlength="8" oninput="invoiceTaxId = this.value.replace(/\D/g,''); this.value = invoiceTaxId;" placeholder="輸入 8 碼公司統一編號"
                class="w-full px-3 py-2 bg-white border border-neutral-300 rounded-lg text-xs font-mono focus:outline-none focus:border-neutral-900" />
            </div>
          </div>

          <!-- 費用明細 -->
          <div class="border-t border-neutral-200 pt-4 space-y-2 text-sm">
            <div class="flex justify-between text-neutral-600"><span>餐點小計</span><span id="sum-subtotal" class="font-medium text-neutral-900">$0</span></div>
            <div class="flex justify-between text-neutral-600"><span>外送費（<span id="sum-mode-label">外送</span>）</span><span id="sum-delivery" class="font-medium text-neutral-900">$0</span></div>
            <div class="flex justify-between text-neutral-600"><span>平台服務費</span><span id="sum-service" class="font-medium text-neutral-900">$0</span></div>
            <div class="flex justify-between text-[#059652] font-semibold"><span>會員折扣</span><span id="sum-discount">-$0</span></div>
            <div class="flex justify-between text-lg font-extrabold border-t border-neutral-200 pt-3 text-neutral-950">
              <span>應付總額</span>
              <span id="sum-total">$0</span>
            </div>
          </div>

          <button id="checkout-btn" type="button" onclick="initiateCheckout()"
            class="w-full py-3.5 bg-[#06C167] hover:bg-[#05a858] disabled:bg-neutral-300 disabled:text-neutral-500 text-neutral-950 font-extrabold text-sm rounded-xl transition cursor-pointer shadow-sm">
            前往結帳（下一步：確認地址）
          </button>
        </div>
      </div>
    </section>
  </main>

  <!-- ==================== 頁尾 ==================== -->
  <footer class="border-t border-neutral-100 mt-12 py-6 text-center text-xs text-neutral-400">
    FoodOrder 美味快點｜智慧點餐管理系統 • 支援 Google 地圖地址標記、電子發票載具與多元支付
  </footer>

  <!-- ==================== 餐廳菜單 Modal ==================== -->
  <div id="menu-modal" role="dialog" aria-modal="true" aria-labelledby="modal-rest-name"
    class="hidden fixed inset-0 bg-black/60 backdrop-blur-sm z-40 flex items-end sm:items-center justify-center sm:p-4" onclick="if(event.target===this) closeMenuModal()">
    <div class="bg-white rounded-t-3xl sm:rounded-2xl max-w-3xl w-full max-h-[92vh] flex flex-col overflow-hidden shadow-2xl">
      <!-- 餐廳封面圖與基本資訊 -->
      <div class="relative h-44 sm:h-52 shrink-0 bg-neutral-200">
        <img id="modal-rest-cover" alt="餐廳封面" class="w-full h-full object-cover" />
        <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/30 to-transparent"></div>
        <button type="button" onclick="closeMenuModal()" aria-label="關閉餐廳菜單"
          class="absolute top-4 right-4 w-9 h-9 rounded-full bg-white/90 hover:bg-white text-neutral-900 flex items-center justify-center shadow-md transition cursor-pointer">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/></svg>
        </button>
        <div class="absolute bottom-4 left-5 right-5 text-white">
          <h3 id="modal-rest-name" class="text-xl sm:text-2xl font-extrabold tracking-tight"></h3>
          <p id="modal-rest-meta" class="text-xs text-neutral-200 mt-1"></p>
        </div>
      </div>

      <!-- 餐廳公告列 -->
      <div id="modal-rest-notice" class="px-5 py-2 bg-neutral-50 border-b border-neutral-200 text-xs text-neutral-600 shrink-0 hidden"></div>

      <!-- 餐廳所在地址與 Google 地圖預覽列 -->
      <div class="px-5 py-2.5 bg-white border-b border-neutral-200 shrink-0 space-y-2.5">
        <div class="flex flex-wrap items-center justify-between gap-2 text-xs">
          <div class="flex items-center gap-1.5 text-neutral-700 min-w-0">
            <svg class="w-4 h-4 text-[#059652] shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 21s-6-5.686-6-10a6 6 0 1112 0c0 4.314-6 10-6 10z"/><circle cx="12" cy="11" r="2.5"/>
            </svg>
            <span id="modal-rest-address" class="font-medium truncate">載入餐廳地址中...</span>
          </div>
          <div class="flex items-center gap-2 shrink-0">
            <button id="toggle-rest-map-btn" type="button" onclick="toggleRestaurantMap()"
              class="px-3 py-1 rounded-full bg-emerald-50 hover:bg-emerald-100 text-[#059652] border border-emerald-200 font-semibold transition cursor-pointer">
              查看 Google 地圖
            </button>
            <a id="modal-rest-map-link" href="#" target="_blank" rel="noopener noreferrer"
              class="px-3 py-1 rounded-full bg-neutral-100 hover:bg-neutral-200 text-neutral-700 font-semibold transition">
              開啟導航 ↗
            </a>
          </div>
        </div>
        <div id="modal-rest-map-wrap" class="hidden rounded-xl overflow-hidden border border-neutral-200 bg-neutral-100 h-48">
          <iframe id="modal-rest-map-iframe" title="餐廳 Google 地圖位置" class="w-full h-full border-0" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>

      <!-- 餐點分類篩選 -->
      <div id="meal-category-tabs" class="px-5 py-3 border-b border-neutral-100 flex gap-2 overflow-x-auto no-scrollbar shrink-0 bg-white"></div>

      <!-- 兩欄式餐點列表 -->
      <div id="modal-menu-list" class="p-5 overflow-y-auto grid grid-cols-1 sm:grid-cols-2 gap-4 safe-bottom bg-neutral-50/40"></div>
    </div>
  </div>

  <!-- ==================== 餐點客製化 Modal ==================== -->
  <div id="custom-modal" role="dialog" aria-modal="true" aria-labelledby="custom-item-name"
    class="hidden fixed inset-0 bg-black/65 backdrop-blur-sm z-50 flex items-end sm:items-center justify-center sm:p-4" onclick="if(event.target===this) closeCustomModal()">
    <div class="bg-white rounded-t-3xl sm:rounded-2xl max-w-md w-full max-h-[90vh] flex flex-col overflow-hidden shadow-2xl">
      <div class="relative h-40 shrink-0 bg-neutral-100">
        <img id="custom-item-img" alt="餐點圖片" class="w-full h-full object-cover" />
        <button type="button" onclick="closeCustomModal()" aria-label="關閉客製化視窗"
          class="absolute top-3 right-3 w-8 h-8 rounded-full bg-white/90 hover:bg-white text-neutral-900 flex items-center justify-center shadow cursor-pointer">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/></svg>
        </button>
      </div>

      <div class="p-5 overflow-y-auto space-y-4">
        <div>
          <h3 id="custom-item-name" class="font-extrabold text-lg text-neutral-950"></h3>
          <p id="custom-item-desc" class="text-xs text-neutral-500 mt-0.5"></p>
          <p id="custom-item-price" class="text-sm font-bold text-[#059652] mt-1"></p>
        </div>

        <!-- 冰塊與甜度（非飲料自動禁用） -->
        <div id="custom-drink-options" class="grid grid-cols-2 gap-3 text-xs">
          <div>
            <label for="custom-ice" class="block font-bold text-neutral-700 mb-1">冰塊調整</label>
            <select id="custom-ice" class="w-full border border-neutral-300 rounded-xl px-3 py-2 bg-white disabled:bg-neutral-100 disabled:text-neutral-400">
              <option>正常冰</option><option>少冰</option><option>微冰</option><option>去冰</option><option>熱飲／不適用</option>
            </select>
          </div>
          <div>
            <label for="custom-sugar" class="block font-bold text-neutral-700 mb-1">甜度調整</label>
            <select id="custom-sugar" class="w-full border border-neutral-300 rounded-xl px-3 py-2 bg-white disabled:bg-neutral-100 disabled:text-neutral-400">
              <option>正常糖</option><option>少糖</option><option>半糖</option><option>微糖</option><option>無糖／不適用</option>
            </select>
          </div>
        </div>
        <p id="custom-drink-hint" class="hidden text-[11px] text-neutral-400 -mt-2">此餐點非飲品類別，無需調整冰塊與甜度。</p>

        <!-- 依餐廳分類提供合理配料 -->
        <div class="space-y-2 text-xs">
          <span class="block font-bold text-neutral-700">精選加料客製化</span>
          <div id="custom-addons" class="grid grid-cols-2 gap-2"></div>
        </div>

        <!-- 餐點備註 -->
        <div class="space-y-1 text-xs">
          <label for="custom-note" class="block font-bold text-neutral-700">餐點備註（選填）</label>
          <input id="custom-note" type="text" maxlength="50" placeholder="例如：不要香菜、醬料分開、餐具兩份..."
            class="w-full border border-neutral-300 rounded-xl px-3 py-2 focus:outline-none focus:border-neutral-900" />
        </div>
      </div>

      <!-- 底部數量與加入購物車 -->
      <div class="p-4 border-t border-neutral-100 bg-neutral-50 flex items-center gap-3 shrink-0 safe-bottom">
        <div class="flex items-center border border-neutral-300 rounded-xl bg-white">
          <button type="button" onclick="adjustCustomQty(-1)" aria-label="減少數量" class="w-9 h-9 font-bold text-lg hover:bg-neutral-100 rounded-l-xl cursor-pointer">−</button>
          <span id="custom-qty-display" class="w-8 text-center text-sm font-bold">1</span>
          <button type="button" onclick="adjustCustomQty(1)" aria-label="增加數量" class="w-9 h-9 font-bold text-lg hover:bg-neutral-100 rounded-r-xl cursor-pointer">+</button>
        </div>
        <button type="button" onclick="confirmAddToCart()" class="flex-1 py-2.5 bg-neutral-950 hover:bg-neutral-800 text-white font-bold text-sm rounded-xl transition cursor-pointer">
          加入購物車 • <span id="custom-btn-total">$0</span>
        </button>
      </div>
    </div>
  </div>

  <!-- ==================== FoodOrder One 會員管理 Modal ==================== -->
  <div id="vip-modal" role="dialog" aria-modal="true" aria-labelledby="vip-modal-title"
    class="hidden fixed inset-0 bg-black/65 backdrop-blur-sm z-50 flex items-center justify-center p-4" onclick="if(event.target===this) closeVipModal()">
    <div class="bg-white rounded-2xl max-w-md w-full overflow-hidden shadow-2xl border border-neutral-200">
      <div class="bg-neutral-950 text-white p-6 relative">
        <button type="button" onclick="closeVipModal()" aria-label="關閉會員視窗" class="absolute top-4 right-4 text-neutral-400 hover:text-white cursor-pointer">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/></svg>
        </button>
        <span class="text-xs font-bold text-[#06C167] tracking-wider uppercase">FoodOrder One</span>
        <h3 id="vip-modal-title" class="text-xl font-extrabold mt-1">尊榮會員方案管理</h3>
        <p class="text-xs text-neutral-300 mt-1">月費 $120，隨時可免費取消訂閱</p>
      </div>
      <div class="p-6 space-y-4 text-sm">
        <ul class="space-y-2 text-xs text-neutral-700">
          <li class="flex items-center gap-2"><span class="text-[#06C167] font-bold">✓</span> 所有外送訂單享 <b>$0 外送費</b>（原價 $39）</li>
          <li class="flex items-center gap-2"><span class="text-[#06C167] font-bold">✓</span> 全站免收 <b>$15 平台服務費</b></li>
          <li class="flex items-center gap-2"><span class="text-[#06C167] font-bold">✓</span> 獨享專屬折扣碼 <b>PRO85（85折）</b> 與 <b>VIP50（現折$50）</b></li>
        </ul>
        <div id="vip-modal-actions" class="pt-2 space-y-2"></div>
      </div>
    </div>
  </div>

  <!-- ==================== 登入與帳號管理 Modal ==================== -->
  <div id="login-modal" role="dialog" aria-modal="true" aria-labelledby="login-modal-title"
    class="hidden fixed inset-0 bg-black/65 backdrop-blur-sm z-50 flex items-center justify-center p-4" onclick="if(event.target===this) closeLoginModal()">
    <div class="bg-white rounded-2xl max-w-md w-full max-h-[90vh] overflow-y-auto shadow-2xl border border-neutral-200 p-6 space-y-5">
      <div class="flex items-center justify-between">
        <h3 id="login-modal-title" class="text-lg font-extrabold text-neutral-950">會員登入</h3>
        <button type="button" onclick="closeLoginModal()" aria-label="關閉登入視窗" class="w-8 h-8 rounded-full hover:bg-neutral-100 flex items-center justify-center cursor-pointer">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/></svg>
        </button>
      </div>

      <!-- 未登入表單 -->
      <div id="login-guest-view" class="space-y-4">
        <!-- Google 登入按鈕 -->
        <button type="button" onclick="openGoogleOAuthModal('login')"
          class="w-full py-2.5 px-4 bg-white hover:bg-neutral-50 border border-neutral-300 rounded-xl flex items-center justify-center gap-2.5 text-sm font-semibold text-neutral-800 transition cursor-pointer shadow-sm">
          <svg class="w-5 h-5" viewBox="0 0 24 24">
            <path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/>
            <path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/>
            <path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"/>
            <path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"/>
          </svg>
          使用 Google 帳戶繼續
        </button>

        <div class="relative flex items-center justify-center">
          <div class="border-t border-neutral-200 w-full"></div>
          <span class="bg-white px-3 text-[11px] text-neutral-400 shrink-0">或使用帳號登入</span>
          <div class="border-t border-neutral-200 w-full"></div>
        </div>

        <div class="space-y-3 text-sm">
          <div>
            <label for="login-username" class="block text-xs font-bold text-neutral-700 mb-1">登入帳號（英數字或底線 3~20 碼）</label>
            <input id="login-username" type="text" placeholder="例如：student01"
              onkeydown="if(event.key==='Enter') submitLogin()"
              class="w-full px-3.5 py-2.5 border border-neutral-300 rounded-xl focus:outline-none focus:border-neutral-900" />
          </div>
          <div>
            <label for="login-display" class="block text-xs font-bold text-neutral-700 mb-1">顯示名稱（首次登入選填）</label>
            <input id="login-display" type="text" placeholder="例如：王小明"
              onkeydown="if(event.key==='Enter') submitLogin()"
              class="w-full px-3.5 py-2.5 border border-neutral-300 rounded-xl focus:outline-none focus:border-neutral-900" />
          </div>
        </div>

        <div class="space-y-2">
          <button type="button" onclick="submitLogin()" class="w-full py-2.5 bg-neutral-950 hover:bg-neutral-800 text-white rounded-xl text-sm font-bold transition cursor-pointer">
            立即登入
          </button>
          <button type="button" onclick="quickDemoLogin()" class="w-full py-2 bg-neutral-100 hover:bg-neutral-200 text-neutral-800 rounded-xl text-xs font-semibold transition cursor-pointer">
            一鍵使用示範帳號登入（王小明 / student01）
          </button>
        </div>

        <!-- 下方註冊入口 -->
        <div class="pt-3 border-t border-neutral-100 text-center text-xs text-neutral-500">
          還沒有帳號嗎？
          <button type="button" onclick="openRegisterModal()" class="font-bold text-[#059652] hover:underline ml-1 cursor-pointer">
            註冊？立即建立新帳號
          </button>
        </div>
      </div>

      <!-- 已登入帳號管理頁 -->
      <div id="login-authed-view" class="hidden space-y-4">
        <!-- 會員頭像與基本摘要 -->
        <div class="p-4 rounded-xl bg-neutral-50 border border-neutral-200 flex items-center gap-3.5">
          <div id="acct-avatar-circle" class="w-12 h-12 rounded-full bg-neutral-900 text-white font-extrabold text-lg flex items-center justify-center shrink-0">
            U
          </div>
          <div class="min-w-0 flex-1">
            <div class="flex items-center justify-between gap-2">
              <p id="acct-display-name" class="font-extrabold text-base text-neutral-950 truncate"></p>
              <span id="acct-vip-tag" class="text-[11px] font-bold px-2.5 py-0.5 rounded-full shrink-0"></span>
            </div>
            <p id="acct-username" class="text-xs text-neutral-500 mt-0.5"></p>
          </div>
        </div>

        <!-- 分頁切換：個人資料修改 / 帳號與載具綁定 -->
        <div class="grid grid-cols-2 bg-neutral-100 p-1 rounded-xl text-xs font-bold">
          <button id="acct-tab-profile" type="button" onclick="switchAccountTab('profile')" class="py-2 rounded-lg transition cursor-pointer">
            個人資料設定
          </button>
          <button id="acct-tab-bindings" type="button" onclick="switchAccountTab('bindings')" class="py-2 rounded-lg transition cursor-pointer">
            Google 與載具綁定
          </button>
        </div>

        <!-- 分頁 1：直接修改姓名、電話、生日、地址 -->
        <div id="acct-panel-profile" class="space-y-3 text-xs">
          <div>
            <label for="acct-edit-name" class="block font-bold text-neutral-700 mb-1">姓名 / 顯示名稱 *</label>
            <input id="acct-edit-name" type="text" maxlength="30" placeholder="請輸入姓名"
              class="w-full px-3.5 py-2.5 bg-neutral-50 focus:bg-white border border-neutral-300 rounded-xl text-sm focus:outline-none focus:border-neutral-900" />
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
            <div>
              <label for="acct-edit-phone" class="block font-bold text-neutral-700 mb-1">手機電話</label>
              <input id="acct-edit-phone" type="tel" maxlength="10" placeholder="09xxxxxxxx"
                class="w-full px-3.5 py-2.5 bg-neutral-50 focus:bg-white border border-neutral-300 rounded-xl text-sm focus:outline-none focus:border-neutral-900" />
            </div>
            <div>
              <label for="acct-edit-birthday" class="block font-bold text-neutral-700 mb-1">出生日期</label>
              <input id="acct-edit-birthday" type="date"
                class="w-full px-3.5 py-2.5 bg-neutral-50 focus:bg-white border border-neutral-300 rounded-xl text-sm focus:outline-none focus:border-neutral-900" />
            </div>
          </div>

          <div>
            <div class="flex items-center justify-between mb-1">
              <label for="acct-edit-address" class="font-bold text-neutral-700">預設外送地址 *</label>
              <button type="button" onclick="openMapFromProfileEdit()" class="text-[11px] font-bold text-[#059652] hover:underline cursor-pointer">
                從 Google 地圖標記 ↗
              </button>
            </div>
            <input id="acct-edit-address" type="text" maxlength="100" placeholder="例如：台中市霧峰區中正路800號"
              class="w-full px-3.5 py-2.5 bg-neutral-50 focus:bg-white border border-neutral-300 rounded-xl text-sm focus:outline-none focus:border-neutral-900" />
          </div>

          <div>
            <label for="acct-edit-address-note" class="block font-bold text-neutral-700 mb-1">預設門牌 / 樓層備註（選填）</label>
            <input id="acct-edit-address-note" type="text" maxlength="60" placeholder="例如：3樓 302 室、放警衛室..."
              class="w-full px-3.5 py-2.5 bg-neutral-50 focus:bg-white border border-neutral-300 rounded-xl text-sm focus:outline-none focus:border-neutral-900" />
          </div>

          <button type="button" onclick="saveAccountProfile()" class="w-full py-2.5 bg-[#06C167] hover:bg-[#05a858] text-neutral-950 rounded-xl text-sm font-extrabold transition cursor-pointer shadow-sm">
            儲存個人資料變更
          </button>
        </div>

        <!-- 分頁 2：Google 帳號與手機條碼載具綁定 -->
        <div id="acct-panel-bindings" class="hidden space-y-3">
          <div class="p-4 rounded-xl border border-neutral-200 space-y-2">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold text-neutral-800">Google 帳號繫結</span>
              <span id="acct-google-status" class="text-[11px] font-semibold"></span>
            </div>
            <p id="acct-google-email" class="text-xs text-neutral-500"></p>
            <div id="acct-google-actions"></div>
          </div>

          <div class="p-4 rounded-xl border border-neutral-200 space-y-2.5">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold text-neutral-800">手機條碼載具綁定</span>
              <span id="acct-carrier-status" class="text-[11px] font-semibold"></span>
            </div>
            <div class="flex gap-2">
              <input id="acct-carrier-input" type="text" maxlength="8" oninput="formatCarrierInput(this)" placeholder="輸入手機條碼（如 /AB12345）"
                class="flex-1 px-3 py-2 bg-neutral-50 border border-neutral-300 rounded-lg text-xs font-mono uppercase focus:outline-none focus:border-neutral-900" />
              <button type="button" onclick="saveAccountCarrier()" class="px-3 py-2 bg-neutral-900 hover:bg-neutral-800 text-white rounded-lg text-xs font-semibold cursor-pointer shrink-0">
                儲存綁定
              </button>
            </div>
            <button id="acct-carrier-unbind-btn" type="button" onclick="unbindAccountCarrier()" class="hidden text-[11px] font-semibold text-red-600 hover:underline cursor-pointer">
              解除載具綁定
            </button>
          </div>
        </div>

        <button type="button" onclick="logoutUser()" class="w-full py-2.5 bg-red-50 hover:bg-red-100 text-red-600 font-bold text-sm rounded-xl transition cursor-pointer">
          登出目前帳號
        </button>
      </div>
    </div>
  </div>

  <!-- ==================== 三步驟會員註冊 Modal ==================== -->
  <div id="register-modal" role="dialog" aria-modal="true" aria-labelledby="reg-modal-title"
    class="hidden fixed inset-0 bg-black/65 backdrop-blur-sm z-50 flex items-center justify-center p-4" onclick="if(event.target===this) closeRegisterModal()">
    <div class="bg-white rounded-2xl max-w-md w-full overflow-hidden shadow-2xl border border-neutral-200">
      <div class="px-6 pt-5 pb-4 border-b border-neutral-100 flex items-start justify-between">
        <div>
          <span id="reg-step-badge" class="inline-block text-[11px] font-bold text-[#059652] bg-emerald-50 border border-emerald-200 px-2.5 py-0.5 rounded-full">步驟 1 / 3</span>
          <h3 id="reg-modal-title" class="text-lg font-extrabold text-neutral-950 mt-1.5">建立新帳號：綁定基本資料</h3>
        </div>
        <button type="button" onclick="closeRegisterModal()" aria-label="關閉註冊視窗" class="w-8 h-8 rounded-full hover:bg-neutral-100 flex items-center justify-center cursor-pointer">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/></svg>
        </button>
      </div>

      <!-- 進度條 -->
      <div class="px-6 pt-3 grid grid-cols-3 gap-2">
        <div id="reg-bar-1" class="h-1.5 rounded-full bg-[#06C167]"></div>
        <div id="reg-bar-2" class="h-1.5 rounded-full bg-neutral-200"></div>
        <div id="reg-bar-3" class="h-1.5 rounded-full bg-neutral-200"></div>
      </div>

      <div class="p-6">
        <!-- 步驟 1：姓名、生日、電話 -->
        <div id="reg-step-1" class="space-y-3 text-sm">
          <div>
            <label class="block text-xs font-bold text-neutral-700 mb-1">登入帳號 *</label>
            <input id="reg-username" type="text" placeholder="英數字或底線 3~20 碼（例如：amy_2026）" class="w-full px-3.5 py-2 border border-neutral-300 rounded-xl focus:outline-none focus:border-neutral-900" />
          </div>
          <div>
            <label class="block text-xs font-bold text-neutral-700 mb-1">真實姓名 *</label>
            <input id="reg-name" type="text" placeholder="請輸入姓名" class="w-full px-3.5 py-2 border border-neutral-300 rounded-xl focus:outline-none focus:border-neutral-900" />
          </div>
          <div>
            <label class="block text-xs font-bold text-neutral-700 mb-1">出生日期 *</label>
            <input id="reg-birthday" type="date" class="w-full px-3.5 py-2 border border-neutral-300 rounded-xl focus:outline-none focus:border-neutral-900" />
          </div>
          <div>
            <label class="block text-xs font-bold text-neutral-700 mb-1">手機號碼 *</label>
            <input id="reg-phone" type="tel" maxlength="10" placeholder="09xxxxxxxx（10 碼）" class="w-full px-3.5 py-2 border border-neutral-300 rounded-xl focus:outline-none focus:border-neutral-900" />
          </div>
          <button type="button" onclick="nextRegStep1()" class="w-full mt-2 py-2.5 bg-neutral-950 hover:bg-neutral-800 text-white rounded-xl font-bold cursor-pointer">
            下一步：信用卡設定
          </button>
        </div>

        <!-- 步驟 2：是否新增信用卡（可跳過） -->
        <div id="reg-step-2" class="hidden space-y-3 text-sm">
          <p class="text-xs text-neutral-500">綁定常用信用卡可加速結帳流程（支援 Visa / Mastercard / JCB），此步驟可先跳過。</p>
          <div class="relative">
            <input id="reg-card-number" type="text" maxlength="19" oninput="formatRegCardNumber(this)" placeholder="信用卡卡號（選填）"
              class="w-full px-3.5 py-2.5 border border-neutral-300 rounded-xl font-mono text-xs focus:outline-none focus:border-neutral-900" />
            <span id="reg-card-brand" class="absolute right-3 top-1/2 -translate-y-1/2 text-[11px] font-extrabold text-neutral-400"></span>
          </div>
          <div class="grid grid-cols-2 gap-2">
            <input id="reg-card-expiry" type="text" maxlength="5" oninput="formatCardExpiry(this)" placeholder="有效期限 MM/YY"
              class="px-3.5 py-2.5 border border-neutral-300 rounded-xl font-mono text-xs focus:outline-none focus:border-neutral-900" />
            <input id="reg-card-cvv" type="password" maxlength="4" placeholder="安全碼 CVV"
              class="px-3.5 py-2.5 border border-neutral-300 rounded-xl font-mono text-xs focus:outline-none focus:border-neutral-900" />
          </div>
          <div class="space-y-2 pt-2">
            <button type="button" onclick="nextRegStep2(false)" class="w-full py-2.5 bg-neutral-950 hover:bg-neutral-800 text-white rounded-xl font-bold cursor-pointer">
              綁定信用卡並繼續
            </button>
            <button type="button" onclick="nextRegStep2(true)" class="w-full py-2 bg-neutral-100 hover:bg-neutral-200 text-neutral-700 rounded-xl text-xs font-semibold cursor-pointer">
              暫時不新增，跳過此步驟
            </button>
          </div>
        </div>

        <!-- 步驟 3：是否開啟定位 -->
        <div id="reg-step-3" class="hidden space-y-4 text-center">
          <div class="w-14 h-14 mx-auto rounded-2xl bg-emerald-50 text-[#059652] flex items-center justify-center">
            <svg class="w-8 h-8" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 21s-6-5.686-6-10a6 6 0 1112 0c0 4.314-6 10-6 10z"/><circle cx="12" cy="11" r="2.5"/>
            </svg>
          </div>
          <div class="space-y-1">
            <h4 class="font-extrabold text-base text-neutral-950">是否開啟即時定位服務？</h4>
            <p class="text-xs text-neutral-500">開啟定位可自動帶入您附近的外送地址與估算精準送達時間。</p>
          </div>
          <div class="space-y-2 pt-1">
            <button type="button" onclick="finishRegistration(true)" class="w-full py-2.5 bg-[#06C167] hover:bg-[#05a858] text-neutral-950 rounded-xl font-extrabold text-sm cursor-pointer">
              開啟定位並完成註冊
            </button>
            <button type="button" onclick="finishRegistration(false)" class="w-full py-2 bg-neutral-100 hover:bg-neutral-200 text-neutral-700 rounded-xl text-xs font-semibold cursor-pointer">
              暫不開啟，直接完成註冊
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ==================== 模擬 Google OAuth 帳戶選擇視窗 ==================== -->
  <div id="google-oauth-modal" role="dialog" aria-modal="true" aria-labelledby="google-oauth-title"
    class="hidden fixed inset-0 bg-black/70 backdrop-blur-sm z-50 flex items-center justify-center p-4" onclick="if(event.target===this) closeGoogleOAuthModal()">
    <div class="bg-white rounded-2xl max-w-sm w-full overflow-hidden shadow-2xl border border-neutral-200">
      <div class="p-6 pb-4 text-center border-b border-neutral-100">
        <svg class="w-8 h-8 mx-auto mb-2" viewBox="0 0 24 24">
          <path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/>
          <path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/>
          <path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"/>
          <path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"/>
        </svg>
        <h3 id="google-oauth-title" class="text-base font-bold text-neutral-900">選擇要繼續使用的帳戶</h3>
        <p class="text-xs text-neutral-500 mt-0.5">以繼續使用「FoodOrder 美味快點」</p>
      </div>
      <div class="divide-y divide-neutral-100">
        <button type="button" onclick="selectGoogleAccount('王小明', 'ming.wang@gmail.com')" class="w-full px-6 py-3.5 flex items-center gap-3 hover:bg-neutral-50 text-left cursor-pointer">
          <span class="w-9 h-9 rounded-full bg-blue-600 text-white font-bold flex items-center justify-center text-sm shrink-0">M</span>
          <div class="min-w-0">
            <p class="text-sm font-bold text-neutral-900 truncate">王小明</p>
            <p class="text-xs text-neutral-500 truncate">ming.wang@gmail.com</p>
          </div>
        </button>
        <button type="button" onclick="selectGoogleAccount('林佳穎', 'chia.lin@gmail.com')" class="w-full px-6 py-3.5 flex items-center gap-3 hover:bg-neutral-50 text-left cursor-pointer">
          <span class="w-9 h-9 rounded-full bg-emerald-600 text-white font-bold flex items-center justify-center text-sm shrink-0">C</span>
          <div class="min-w-0">
            <p class="text-sm font-bold text-neutral-900 truncate">林佳穎</p>
            <p class="text-xs text-neutral-500 truncate">chia.lin@gmail.com</p>
          </div>
        </button>
        <div class="p-4 space-y-2">
          <input id="custom-google-email" type="email" placeholder="或輸入其他 Gmail 帳號..." class="w-full px-3 py-2 border border-neutral-300 rounded-lg text-xs focus:outline-none focus:border-blue-600" />
          <button type="button" onclick="submitCustomGoogleAccount()" class="w-full py-2 bg-blue-600 hover:bg-blue-700 text-white rounded-lg text-xs font-bold cursor-pointer">
            使用此 Gmail 繼續
          </button>
        </div>
      </div>
      <div class="px-6 py-3.5 bg-neutral-50 border-t border-neutral-100 flex items-center justify-between text-xs">
        <span class="text-neutral-400">OAuth 2.0 授權模擬</span>
        <button type="button" onclick="closeGoogleOAuthModal()" class="font-semibold text-neutral-600 hover:text-neutral-900 cursor-pointer">取消</button>
      </div>
    </div>
  </div>

  <!-- ==================== 確認配送地址與 Google 地圖標記 Modal（步驟 1/2） ==================== -->
  <div id="address-modal" role="dialog" aria-modal="true" aria-labelledby="address-modal-title"
    class="hidden fixed inset-0 bg-black/65 backdrop-blur-sm z-50 flex items-center justify-center p-4" onclick="if(event.target===this) closeAddressModal()">
    <div class="bg-white rounded-2xl max-w-lg w-full max-h-[92vh] flex flex-col overflow-hidden shadow-2xl border border-neutral-200">
      <div class="px-6 pt-5 pb-4 border-b border-neutral-100 flex items-start justify-between gap-3 shrink-0">
        <div>
          <span id="address-step-badge" class="inline-flex items-center gap-1.5 text-xs font-bold text-[#059652] bg-emerald-50 border border-emerald-200 px-2.5 py-0.5 rounded-full">
            步驟 1/2 • 確認地址
          </span>
          <h3 id="address-modal-title" class="text-lg font-bold text-neutral-950 mt-1.5">確認外送地址並於地圖標記</h3>
          <p id="address-modal-subtitle" class="text-xs text-neutral-500 mt-0.5">請確認餐點送達地址，下方 Google 地圖將即時標出精確位置</p>
        </div>
        <button type="button" onclick="closeAddressModal()" aria-label="關閉地址確認視窗"
          class="w-8 h-8 rounded-full hover:bg-neutral-100 text-neutral-500 hover:text-neutral-900 flex items-center justify-center transition cursor-pointer shrink-0">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/>
          </svg>
        </button>
      </div>

      <div class="p-6 overflow-y-auto space-y-4">
        <!-- 外送地址輸入與快選區 -->
        <div id="address-delivery-controls" class="space-y-3">
          <div class="space-y-1.5">
            <label for="address-input" class="text-xs font-bold text-neutral-700 block">外送地址</label>
            <div class="flex gap-2">
              <input id="address-input" type="text" placeholder="請輸入完整送達地址（例如：台中市霧峰區中正路800號）"
                onkeydown="if(event.key==='Enter'){ event.preventDefault(); pinAddressOnMap(); }"
                class="flex-1 px-3.5 py-2.5 bg-white border border-neutral-300 rounded-xl text-sm focus:outline-none focus:border-neutral-900" />
              <button type="button" onclick="pinAddressOnMap()"
                class="px-4 py-2.5 bg-neutral-900 hover:bg-neutral-800 text-white rounded-xl text-xs font-semibold transition cursor-pointer shrink-0">
                標記地圖
              </button>
            </div>
          </div>

          <!-- 常用地點快選與 GPS 定位 -->
          <div class="flex flex-wrap items-center gap-1.5 text-[11px]">
            <button type="button" onclick="useGpsForAddress()" class="px-2.5 py-1 rounded-full bg-emerald-50 hover:bg-emerald-100 text-[#059652] border border-emerald-200 font-semibold transition cursor-pointer">
              使用目前定位
            </button>
            <button type="button" onclick="applyPresetAddress('台中市霧峰區吉峰東路168號')" class="px-2.5 py-1 rounded-full bg-neutral-100 hover:bg-neutral-200 text-neutral-700 font-medium cursor-pointer">朝陽科大</button>
            <button type="button" onclick="applyPresetAddress('台中市霧峰區柳豐路500號')" class="px-2.5 py-1 rounded-full bg-neutral-100 hover:bg-neutral-200 text-neutral-700 font-medium cursor-pointer">亞洲大學</button>
            <button type="button" onclick="applyPresetAddress('台中市霧峰區中正路800號')" class="px-2.5 py-1 rounded-full bg-neutral-100 hover:bg-neutral-200 text-neutral-700 font-medium cursor-pointer">霧峰中正路</button>
            <button type="button" onclick="applyPresetAddress('台中市大里區中興路二段200號')" class="px-2.5 py-1 rounded-full bg-neutral-100 hover:bg-neutral-200 text-neutral-700 font-medium cursor-pointer">大里中興路</button>
          </div>

          <!-- 樓層 / 門牌備註 -->
          <div>
            <label for="address-note-input" class="text-xs font-bold text-neutral-700 block mb-1">門牌／樓層與外送員備註（選填）</label>
            <input id="address-note-input" type="text" maxlength="60" placeholder="例如：3樓 302 室、放警衛室、抵達請來電..."
              class="w-full px-3.5 py-2 bg-neutral-50 focus:bg-white border border-neutral-300 rounded-xl text-xs focus:outline-none focus:border-neutral-900" />
          </div>
        </div>

        <!-- 自取模式門市資訊 -->
        <div id="address-pickup-info" class="hidden p-3.5 rounded-xl bg-neutral-50 border border-neutral-200 space-y-1">
          <p class="text-xs font-bold text-neutral-900" id="pickup-store-name"></p>
          <p class="text-xs text-neutral-600" id="pickup-store-address"></p>
        </div>

        <!-- Google Maps 內嵌地圖標記預覽 -->
        <div class="space-y-1.5">
          <div class="flex items-center justify-between text-xs">
            <span class="font-bold text-neutral-700">Google 地圖標記位置</span>
            <a id="address-external-map-link" href="#" target="_blank" rel="noopener noreferrer" class="text-[#059652] hover:underline font-semibold">
              在 Google Maps 開啟 ↗
            </a>
          </div>
          <div class="rounded-xl overflow-hidden border border-neutral-200 bg-neutral-100 h-56 relative">
            <iframe id="address-map-iframe" title="Google 地圖標記位置" class="w-full h-full border-0" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
          <p id="address-pinned-label" class="text-[11px] text-neutral-500 truncate"></p>
        </div>
      </div>

      <div class="px-6 py-4 border-t border-neutral-100 bg-neutral-50 flex gap-2.5 shrink-0">
        <button type="button" onclick="closeAddressModal()" class="flex-1 py-2.5 bg-white border border-neutral-300 hover:bg-neutral-100 text-neutral-800 rounded-xl text-sm font-semibold transition cursor-pointer">
          返回
        </button>
        <button id="address-confirm-btn" type="button" onclick="confirmAddressStep()" class="flex-1 py-2.5 bg-[#06C167] hover:bg-[#05a858] text-neutral-950 rounded-xl text-sm font-bold transition cursor-pointer shadow-sm">
          確認地址，下一步
        </button>
      </div>
    </div>
  </div>

  <!-- ==================== 結帳二次確認 Modal（步驟 2/2） ==================== -->
  <div id="checkout-confirm-modal" role="dialog" aria-modal="true" aria-labelledby="checkout-confirm-title"
    class="hidden fixed inset-0 bg-black/65 backdrop-blur-sm z-50 flex items-center justify-center p-4" onclick="if(event.target===this) closeCheckoutConfirmModal()">
    <div class="bg-white rounded-2xl max-w-md w-full overflow-hidden shadow-2xl border border-neutral-200">
      <div class="px-6 pt-6 pb-4 border-b border-neutral-100 flex items-start justify-between gap-3">
        <div>
          <span class="inline-flex items-center gap-1.5 text-xs font-bold text-[#059652] bg-emerald-50 border border-emerald-200 px-2.5 py-0.5 rounded-full">
            步驟 2/2 • 最後確認
          </span>
          <h3 id="checkout-confirm-title" class="text-lg font-bold text-neutral-950 mt-2">確定送出這筆訂單嗎？</h3>
          <p class="text-xs text-neutral-500 mt-0.5">送出後將立即通知餐廳開始備餐，請再次核對以下明細</p>
        </div>
        <button type="button" onclick="closeCheckoutConfirmModal()" aria-label="關閉確認視窗"
          class="w-8 h-8 rounded-full hover:bg-neutral-100 text-neutral-500 hover:text-neutral-900 flex items-center justify-center transition cursor-pointer shrink-0">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/>
          </svg>
        </button>
      </div>

      <div class="p-6 space-y-4">
        <div class="bg-neutral-50 border border-neutral-200 rounded-xl p-4 space-y-2.5 text-xs">
          <div class="flex justify-between gap-2">
            <span class="text-neutral-500">取餐方式</span>
            <span id="confirm-delivery-mode" class="font-bold text-neutral-900"></span>
          </div>
          <div class="flex justify-between items-start gap-2">
            <span id="confirm-address-title" class="text-neutral-500 shrink-0">外送地址</span>
            <div class="text-right min-w-0">
              <p id="confirm-address-text" class="font-bold text-neutral-900 break-words"></p>
              <button type="button" onclick="reopenAddressFromConfirm()" class="text-[11px] text-[#059652] hover:underline font-semibold cursor-pointer">修改地址 / 查看地圖</button>
            </div>
          </div>
          <div class="flex justify-between gap-2">
            <span class="text-neutral-500">付款方式</span>
            <span id="confirm-payment-label" class="font-bold text-neutral-900"></span>
          </div>
          <div class="flex justify-between gap-2">
            <span class="text-neutral-500">電子發票</span>
            <span id="confirm-invoice-label" class="font-bold text-neutral-900"></span>
          </div>
          <div id="confirm-promo-row" class="hidden justify-between gap-2">
            <span class="text-neutral-500">套用優惠</span>
            <span id="confirm-promo-label" class="font-bold text-[#059652]"></span>
          </div>
        </div>

        <div id="confirm-items-preview" class="max-h-36 overflow-y-auto space-y-1.5 text-xs border-t border-b border-neutral-100 py-3"></div>

        <div class="flex items-center justify-between">
          <span class="text-sm font-bold text-neutral-700">應付總金額</span>
          <span id="confirm-total-amount" class="text-xl font-extrabold text-neutral-950"></span>
        </div>

        <div class="flex gap-2.5 pt-1">
          <button type="button" onclick="closeCheckoutConfirmModal()" class="flex-1 py-2.5 bg-neutral-100 hover:bg-neutral-200 text-neutral-800 rounded-xl text-sm font-semibold cursor-pointer">
            返回檢查
          </button>
          <button type="button" onclick="confirmAndSubmitOrder()" class="flex-1 py-2.5 bg-[#06C167] hover:bg-[#05a858] text-neutral-950 rounded-xl text-sm font-extrabold cursor-pointer shadow-sm">
            確定送出訂單
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Toast 通知（支援選配 Undo 動作） -->
  <div id="toast" class="hidden fixed bottom-6 right-6 z-50 bg-neutral-950 text-white px-4 py-3 rounded-xl shadow-2xl text-xs font-medium flex items-center gap-3 max-w-sm">
    <span id="toast-msg"></span>
    <button id="toast-action-btn" type="button" class="hidden text-[#06C167] font-bold hover:underline shrink-0 cursor-pointer"></button>
  </div>

  <script>
    // ==========================================
    // 1. 全域常數與費率設定
    // ==========================================
    const STORAGE_USERS_KEY = "foodorder_users_v2";
    const STORAGE_CURRENT_KEY = "foodorder_current_user_v2";

    const PRICING = {
      DELIVERY_FEE: 39,
      SERVICE_FEE: 15,
      VIP_PROMO_CODES: {
        PRO85: { type: "percent", value: 0.15, label: "付費會員 85 折" },
        VIP50: { type: "fixed", value: 50, label: "付費會員現折 $50" }
      }
    };

    const REST_CATEGORIES = ["全部", "速食", "披薩", "手搖飲", "日式料理", "甜點咖啡"];
    const MEAL_CATEGORIES = ["全部", "主食", "飲料", "甜點", "套餐"];

    const CATEGORY_ADDONS = {
      "速食": { "加起司": 15, "加煙燻培根": 25, "薯條加大": 20, "加太陽蛋": 15 },
      "披薩": { "升級芝心餅皮": 80, "加雙倍莫札瑞拉起司": 45, "加墨西哥辣椒": 25, "加購烤雞翅": 55 },
      "手搖飲": { "加黑糖珍珠": 10, "加Q彈椰果": 10, "加芝士奶蓋": 20, "加嫩仙草凍": 15 },
      "日式料理": { "加溏心蛋": 25, "加炙燒叉燒": 45, "加麵一份": 30, "加海苔片": 15 },
      "甜點咖啡": { "升級燕麥奶": 20, "加義式濃縮": 20, "加鮮奶油": 15, "加海鹽焦糖醬": 15 }
    };

    const SAVED_CARDS = [
      { id: "card_visa", brand: "VISA", last4: "4242", label: "VISA •••• 4242（常用卡）" },
      { id: "card_mc", brand: "Mastercard", last4: "8819", label: "Mastercard •••• 8819" },
      { id: "card_jcb", brand: "JCB", last4: "3528", label: "JCB •••• 3528" }
    ];

    // ==========================================
    // 2. 模擬資料庫：12 家餐廳（含真實 Google 地圖地址）
    // ==========================================
    const RESTAURANTS = [
      {
        id: "r1",
        name: "漢堡狂熱 Burger Fever",
        category: "速食",
        rating: 4.8,
        reviews: "500+",
        delivery_time: "20–30 分鐘",
        pickup_time: "12–18 分鐘",
        distance: "1.2 公里",
        address: "台中市霧峰區中正路912號",
        min_order: 120,
        hours: "10:30–22:00",
        notice: "餐點均為現點現煎，尖峰時段可能需多等候 5 分鐘。",
        cover: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=900&q=80",
        tags: ["美式漢堡", "手工牛肉", "高人氣"],
        menu: [
          { id: "m101", name: "經典雙層起司牛肉堡", category: "主食", price: 165, desc: "雙層手打安格斯牛肉搭配融化切達起司與特製漢堡醬", img: "https://images.unsplash.com/photo-1550547660-d945f859349?auto=format&fit=crop&w=400&q=80" },
          { id: "m102", name: "酥脆轟炸雞腿排套餐", category: "套餐", price: 230, desc: "含厚切去骨雞腿堡、現炸黃金脆薯與冰鎮可樂", img: "https://images.unsplash.com/photo-1606755962773-d324e0a13086?auto=format&fit=crop&w=400&q=80" },
          { id: "m103", name: "冰鎮黃檸檬氣泡可樂", category: "飲料", price: 45, desc: "沁涼氣泡搭配新鮮現切黃檸檬片", img: "https://images.unsplash.com/photo-1622483767028-3f66f32aef97?auto=format&fit=crop&w=400&q=80" },
          { id: "m104", name: "焦糖肉桂布朗尼", category: "甜點", price: 75, desc: "濃郁 70% 黑巧克力現烤布朗尼，佐香甜肉桂焦糖醬", img: "https://images.unsplash.com/photo-1564355808539-22fda35bed7e?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r2",
        name: "茶語軒手搖專門店",
        category: "手搖飲",
        rating: 4.9,
        reviews: "1,200+",
        delivery_time: "15–25 分鐘",
        pickup_time: "8–12 分鐘",
        distance: "0.8 公里",
        address: "台中市霧峰區樹仁路48號",
        min_order: 80,
        hours: "09:30–21:30",
        notice: "鮮奶飲品均採用台灣小農直送鮮乳，歡迎自訂冰塊與甜度。",
        cover: "https://images.unsplash.com/photo-1558857563-b371033873b8?auto=format&fit=crop&w=900&q=80",
        tags: ["黑糖珍珠", "小農鮮奶", "上班族首選"],
        menu: [
          { id: "m201", name: "黑糖珍珠鮮奶茶", category: "飲料", price: 70, desc: "手炒沖繩黑糖慢熬珍珠搭配台灣小農直送鮮奶", img: "https://images.unsplash.com/photo-1558857563-b371033873b8?auto=format&fit=crop&w=400&q=80" },
          { id: "m202", name: "高山四季春青茶", category: "飲料", price: 40, desc: "嚴選南投高山茶葉現萃，茶湯金黃清香回甘", img: "https://images.unsplash.com/photo-1556679343-c7306c1976bc?auto=format&fit=crop&w=400&q=80" },
          { id: "m203", name: "下午茶雙人分享套組", category: "套餐", price: 180, desc: "任選鮮奶茶兩杯搭配每日限量手作奶酪一份", img: "https://images.unsplash.com/photo-1544787219-7f47ccb76574?auto=format&fit=crop&w=400&q=80" },
          { id: "m204", name: "皇家伯爵茶生乳捲", category: "甜點", price: 85, desc: "淡雅佛手柑茶香蛋糕捲入北海道十勝生乳內餡", img: "https://images.unsplash.com/photo-1578985545062-69928b1d9587?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r3",
        name: "一風堂職人拉麵",
        category: "日式料理",
        rating: 4.7,
        reviews: "800+",
        delivery_time: "25–35 分鐘",
        pickup_time: "15–20 分鐘",
        distance: "1.9 公里",
        address: "台中市大里區德芳南路210號",
        min_order: 150,
        hours: "11:00–21:30",
        notice: "外送拉麵全面採「湯麵分離」包裝，確保麵條 Q 彈口感。",
        cover: "https://images.unsplash.com/photo-1569718212165-3a8278d5f624?auto=format&fit=crop&w=900&q=80",
        tags: ["濃厚豚骨", "日式唐揚雞", "暖胃推薦"],
        menu: [
          { id: "m301", name: "赤丸濃厚豚骨拉麵", category: "主食", price: 260, desc: "慢火熬煮 14 小時豚骨湯頭，搭配炙燒叉燒與特製辣味噌", img: "https://images.unsplash.com/photo-1569718212165-3a8278d5f624?auto=format&fit=crop&w=400&q=80" },
          { id: "m302", name: "極上拉麵豪華套餐", category: "套餐", price: 340, desc: "招牌豚骨拉麵＋酥炸日式唐揚雞＋冷泡玄米茶", img: "https://images.unsplash.com/photo-1557872943-16a5ac26437e?auto=format&fit=crop&w=400&q=80" },
          { id: "m303", name: "宇治抹茶紅豆布丁", category: "甜點", price: 90, desc: "京都宇治抹茶粉手工製作，搭配綿密萬丹紅豆", img: "https://images.unsplash.com/photo-1563805042-7684c019e1cb?auto=format&fit=crop&w=400&q=80" },
          { id: "m304", name: "日式冷泡玄米茶", category: "飲料", price: 55, desc: "無糖清爽解膩，入口散發淡雅炒米香氣", img: "https://images.unsplash.com/photo-1515823064-d6e0c04616a7?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r4",
        name: "日光烘焙咖啡館",
        category: "甜點咖啡",
        rating: 4.8,
        reviews: "420+",
        delivery_time: "20–30 分鐘",
        pickup_time: "10–15 分鐘",
        distance: "1.0 公里",
        address: "台中市霧峰區林森路655號",
        min_order: 100,
        hours: "08:00–19:00",
        notice: "所有酸種麵包與巴斯克蛋糕皆為當日清晨手工烘焙。",
        cover: "https://images.unsplash.com/photo-1509440159596-0249088772ff?auto=format&fit=crop&w=900&q=80",
        tags: ["精品咖啡", "巴斯克蛋糕", "早午餐"],
        menu: [
          { id: "m401", name: "燻鮭魚酪梨酸種吐司", category: "主食", price: 195, desc: "挪威冷燻鮭魚與新鮮熟成酪梨切片，淋上初榨橄欖油", img: "https://images.unsplash.com/photo-1525351484163-7529414344d8?auto=format&fit=crop&w=400&q=80" },
          { id: "m402", name: "巴斯克焦香乳酪蛋糕", category: "甜點", price: 130, desc: "外層焦糖微苦香氣、中心半熟滑順濃郁", img: "https://images.unsplash.com/photo-1533134242443-d4fd215305ad?auto=format&fit=crop&w=400&q=80" },
          { id: "m403", name: "西西里檸檬氣泡美式", category: "飲料", price: 115, desc: "中深焙義式濃縮結合屏東鮮榨檸檬汁與細緻氣泡", img: "https://images.unsplash.com/photo-1517701550927-30cf4ba1dba5?auto=format&fit=crop&w=400&q=80" },
          { id: "m404", name: "悠閒早午餐獨享組", category: "套餐", price: 280, desc: "酸種吐司＋巴斯克乳酪蛋糕＋冰美式咖啡", img: "https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r5",
        name: "炸雞大亨 Crispy King",
        category: "速食",
        rating: 4.6,
        reviews: "650+",
        delivery_time: "20–30 分鐘",
        pickup_time: "12–18 分鐘",
        distance: "1.6 公里",
        address: "台中市霧峰區育群路128號",
        min_order: 120,
        hours: "11:30–23:30",
        notice: "採用透氣防潮紙盒包裝，外送到府依然保持金黃酥脆。",
        cover: "https://images.unsplash.com/photo-1626645738196-c2a7c87a8f58?auto=format&fit=crop&w=900&q=80",
        tags: ["美式炸雞", "宵夜首選", "酥脆多汁"],
        menu: [
          { id: "m501", name: "蒜香脆皮無骨炸雞", category: "主食", price: 150, desc: "嚴選溫體去骨雞腿肉，裹上秘製蒜味焦糖醬汁", img: "https://images.unsplash.com/photo-1626645738196-c2a7c87a8f58?auto=format&fit=crop&w=400&q=80" },
          { id: "m502", name: "雙人狂歡炸雞分享餐", category: "套餐", price: 320, desc: "招牌脆皮炸雞 6 塊＋黃金帶皮脆薯＋古早味紅茶兩杯", img: "https://images.unsplash.com/photo-1562967914-608f82629710?auto=format&fit=crop&w=400&q=80" },
          { id: "m503", name: "蜂蜜芥末帶皮脆薯", category: "甜點", price: 65, desc: "整顆馬鈴薯切塊現炸，附美式蜂蜜芥末沾醬", img: "https://images.unsplash.com/photo-1573080496219-bb080dd4f877?auto=format&fit=crop&w=400&q=80" },
          { id: "m504", name: "古早味決明子冰紅茶", category: "飲料", price: 35, desc: "經典炭焙決明子香氣，清爽解炸物油膩", img: "https://images.unsplash.com/photo-1556679343-c7306c1976bc?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r6",
        name: "鮮果茶研所 Fruit Lab",
        category: "手搖飲",
        rating: 4.7,
        reviews: "390+",
        delivery_time: "15–20 分鐘",
        pickup_time: "8–12 分鐘",
        distance: "0.9 公里",
        address: "台中市霧峰區四德路85號",
        min_order: 80,
        hours: "10:00–21:00",
        notice: "當季新鮮水果每日產地直送，無添加人工果露。",
        cover: "https://images.unsplash.com/photo-1546173159-315724a31696?auto=format&fit=crop&w=900&q=80",
        tags: ["新鮮水果茶", "芝士奶蓋", "清爽低負擔"],
        menu: [
          { id: "m601", name: "滿杯愛文楊枝甘露", category: "飲料", price: 85, desc: "新鮮愛文芒果冰沙搭配滑順西米露與葡萄柚果肉", img: "https://images.unsplash.com/photo-1546173159-315724a31696?auto=format&fit=crop&w=400&q=80" },
          { id: "m602", name: "芝芝巨峰葡萄果粒茶", category: "飲料", price: 80, desc: "現剝多汁巨峰葡萄冰沙覆蓋綿密鹹甜起司奶蓋", img: "https://images.unsplash.com/photo-1513558161293-cdaf765ed2fd?auto=format&fit=crop&w=400&q=80" },
          { id: "m603", name: "鮮果冰茶午茶獨享組", category: "套餐", price: 150, desc: "任選鮮果茶一杯搭配法式酸甜檸檬塔一顆", img: "https://images.unsplash.com/photo-1519915028121-7d3463d20b13?auto=format&fit=crop&w=400&q=80" },
          { id: "m604", name: "法式酸甜檸檬塔", category: "甜點", price: 80, desc: "手工發酵奶油塔皮填入清新檸檬凝乳", img: "https://images.unsplash.com/photo-1519915028121-7d3463d20b13?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r7",
        name: "麥當勞 McDonald's（霧峰中正店）",
        category: "速食",
        rating: 4.8,
        reviews: "2,500+",
        delivery_time: "15–25 分鐘",
        pickup_time: "8–12 分鐘",
        distance: "0.7 公里",
        address: "台中市霧峰區中正路839號",
        min_order: 100,
        hours: "06:00–24:00",
        notice: "餐點皆附紙袋包裝，如需番茄醬、糖醋醬請於備註欄填寫。",
        cover: "https://images.unsplash.com/photo-1551782450-a2132b4ba21d?auto=format&fit=crop&w=900&q=80",
        tags: ["大麥克", "麥克雞塊", "24H人氣"],
        menu: [
          { id: "m701", name: "經典大麥克", category: "主食", price: 78, desc: "雙層純牛肉、經典大麥克醬、切達起司與爽脆生菜", img: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=400&q=80" },
          { id: "m702", name: "勁辣雞腿堡", category: "主食", price: 78, desc: "整塊去骨辣味雞腿排現炸酥脆，搭配新鮮美生菜", img: "https://images.unsplash.com/photo-1606755962773-d324e0a13086?auto=format&fit=crop&w=400&q=80" },
          { id: "m703", name: "10塊麥克雞塊經典套餐", category: "套餐", price: 174, desc: "含10塊麥克雞塊、中包金黃薯條與中杯可口可樂（附糖醋醬）", img: "https://images.unsplash.com/photo-1562967914-608f82629710?auto=format&fit=crop&w=400&q=80" },
          { id: "m704", name: "OREO 冰炫風", category: "甜點", price: 59, desc: "香濃奶香冰淇淋拌入酥脆 OREO 巧克力餅乾碎片", img: "https://images.unsplash.com/photo-1563805042-7684c019e1cb?auto=format&fit=crop&w=400&q=80" },
          { id: "m705", name: "冰鎮可口可樂（大）", category: "飲料", price: 45, desc: "暢快沁涼氣泡，速食必備經典搭配", img: "https://images.unsplash.com/photo-1622483767028-3f66f32aef97?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r8",
        name: "肯德基 KFC（台中大里中興店）",
        category: "速食",
        rating: 4.7,
        reviews: "1,800+",
        delivery_time: "20–30 分鐘",
        pickup_time: "10–15 分鐘",
        distance: "1.4 公里",
        address: "台中市大里區中興路二段186號",
        min_order: 120,
        hours: "10:00–23:00",
        notice: "咔啦脆雞部位由門市隨機搭配，原味蛋撻皆為當日現烤出爐。",
        cover: "https://images.unsplash.com/photo-1513639776629-7b61b0ac49cb?auto=format&fit=crop&w=900&q=80",
        tags: ["咔啦脆雞", "原味蛋撻", "XL套餐"],
        menu: [
          { id: "m801", name: "咔啦脆雞（2塊）", category: "主食", price: 142, desc: "獨家裹粉手工現炸，外皮金黃酥脆、肉質鮮嫩微辣多汁", img: "https://images.unsplash.com/photo-1626645738196-c2a7c87a8f58?auto=format&fit=crop&w=400&q=80" },
          { id: "m802", name: "咔啦雞腿堡 XL 全明星餐", category: "套餐", price: 245, desc: "咔啦雞腿堡＋咔啦脆雞1塊＋香酥脆薯＋原味蛋撻＋中杯百事可樂", img: "https://images.unsplash.com/photo-1562967914-608f82629710?auto=format&fit=crop&w=400&q=80" },
          { id: "m803", name: "原味蛋撻禮盒（6入）", category: "甜點", price: 240, desc: "163層酥脆葡式千層撻皮，搭配濃郁奶蛋香滑嫩內餡", img: "https://images.unsplash.com/photo-1519915028121-7d3463d20b13?auto=format&fit=crop&w=400&q=80" },
          { id: "m804", name: "冰無糖茉莉綠茶", category: "飲料", price: 40, desc: "清新淡雅茉莉花香，搭配炸雞清爽解膩", img: "https://images.unsplash.com/photo-1556679343-c7306c1976bc?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r9",
        name: "摩斯漢堡 MOS Burger",
        category: "速食",
        rating: 4.8,
        reviews: "950+",
        delivery_time: "20–30 分鐘",
        pickup_time: "10–15 分鐘",
        distance: "1.1 公里",
        address: "台中市霧峰區中正路956號",
        min_order: 100,
        hours: "07:00–22:00",
        notice: "米漢堡與紅茶均為現點現做，保證熱騰騰送達。",
        cover: "https://images.unsplash.com/photo-1550547660-d945f859349?auto=format&fit=crop&w=900&q=80",
        tags: ["海洋珍珠堡", "摩斯紅茶", "日式速食"],
        menu: [
          { id: "m901", name: "海洋珍珠堡", category: "主食", price: 85, desc: "嚴選鮮蝦、干貝與花枝炸成海鮮天婦羅，夾入香Q台灣米漢堡", img: "https://images.unsplash.com/photo-1550547660-d945f859349?auto=format&fit=crop&w=400&q=80" },
          { id: "m902", name: "燒肉珍珠堡人氣套餐", category: "套餐", price: 175, desc: "薑燒豬肉米漢堡＋黃金薯條＋大杯冰摩斯紅茶", img: "https://images.unsplash.com/photo-1573080496219-bb080dd4f877?auto=format&fit=crop&w=400&q=80" },
          { id: "m903", name: "冰摩斯紅茶（L）", category: "飲料", price: 45, desc: "經典古早味阿薩姆紅茶，可客製冰塊甜度與加檸檬片", img: "https://images.unsplash.com/photo-1556679343-c7306c1976bc?auto=format&fit=crop&w=400&q=80" },
          { id: "m904", name: "方塊薯餅（3入）", category: "甜點", price: 40, desc: "外酥內軟黃金馬鈴薯方塊，點心首選", img: "https://images.unsplash.com/photo-1573080496219-bb080dd4f877?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r10",
        name: "漢堡王 Burger King（台中大里店）",
        category: "速食",
        rating: 4.7,
        reviews: "1,100+",
        delivery_time: "20–30 分鐘",
        pickup_time: "10–15 分鐘",
        distance: "1.5 公里",
        address: "台中市大里區中興路二段312號",
        min_order: 120,
        hours: "10:00–22:30",
        notice: "招牌華堡採直火炙烤純牛肉，帶獨特煙燻炭香。",
        cover: "https://images.unsplash.com/photo-1586190848861-99aa4a171e90?auto=format&fit=crop&w=900&q=80",
        tags: ["火烤華堡", "花生培根堡", "美式速食"],
        menu: [
          { id: "m1001", name: "經典火烤華堡", category: "主食", price: 139, desc: "100% 純牛肉直火炙烤，搭配新鮮番茄、生菜、洋蔥與酸黃瓜", img: "https://images.unsplash.com/photo-1586190848861-99aa4a171e90?auto=format&fit=crop&w=400&q=80" },
          { id: "m1002", name: "美式花生培根脆雞堡餐", category: "套餐", price: 189, desc: "濃郁顆粒花生醬配香酥培根脆雞堡＋中薯＋中杯百事可樂", img: "https://images.unsplash.com/photo-1606755962773-d324e0a13086?auto=format&fit=crop&w=400&q=80" },
          { id: "m1003", name: "香濃巧克力聖代", category: "甜點", price: 55, desc: "綿密香草霜淇淋淋上濃郁比利時風味巧克力醬", img: "https://images.unsplash.com/photo-1563805042-7684c019e1cb?auto=format&fit=crop&w=400&q=80" },
          { id: "m1004", name: "冰鎮七喜汽水（大）", category: "飲料", price: 45, desc: "清爽檸檬萊姆氣泡飲，搭配火烤漢堡超解膩", img: "https://images.unsplash.com/photo-1622483767028-3f66f32aef97?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r11",
        name: "必勝客 Pizza Hut（霧峰中正店）",
        category: "披薩",
        rating: 4.8,
        reviews: "1,400+",
        delivery_time: "25–35 分鐘",
        pickup_time: "15–20 分鐘",
        distance: "0.9 公里",
        address: "台中市霧峰區中正路1035號",
        min_order: 150,
        hours: "11:00–23:00",
        notice: "所有比薩均為現點現烤，可於客製化選項加購芝心餅皮或雙倍起司。",
        cover: "https://images.unsplash.com/photo-1513104890138-7c749659a591?auto=format&fit=crop&w=900&q=80",
        tags: ["芝心比薩", "個人獨享餐", "聚餐首選"],
        menu: [
          { id: "m1101", name: "超級總匯大比薩（13吋）", category: "主食", price: 580, desc: "美式臘腸、義大利肉腸、火腿、青椒、蘑菇與莫札瑞拉起司", img: "https://images.unsplash.com/photo-1513104890138-7c749659a591?auto=format&fit=crop&w=400&q=80" },
          { id: "m1102", name: "和風章魚燒個人比薩套餐", category: "套餐", price: 189, desc: "章魚燒個人比薩＋黃金和風鱈魚塊＋冰可樂一罐", img: "https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?auto=format&fit=crop&w=400&q=80" },
          { id: "m1103", name: "冰藏原味起司塔（2入）", category: "甜點", price: 120, desc: "法國與紐西蘭雙重乳酪製成，冰涼綿密香濃", img: "https://images.unsplash.com/photo-1533134242443-d4fd215305ad?auto=format&fit=crop&w=400&q=80" },
          { id: "m1104", name: "可口可樂（1.25L 分享瓶）", category: "飲料", price: 50, desc: "聚餐派對必備大瓶裝沁涼可樂", img: "https://images.unsplash.com/photo-1622483767028-3f66f32aef97?auto=format&fit=crop&w=400&q=80" }
        ]
      },
      {
        id: "r12",
        name: "達美樂 Domino's Pizza（大里國光店）",
        category: "披薩",
        rating: 4.7,
        reviews: "980+",
        delivery_time: "25–35 分鐘",
        pickup_time: "15–20 分鐘",
        distance: "1.6 公里",
        address: "台中市大里區國光路二段418號",
        min_order: 150,
        hours: "11:00–23:00",
        notice: "手拍薄脆與帕瑪滋心餅皮皆為門市每日新鮮發酵製作。",
        cover: "https://images.unsplash.com/photo-1574071318508-1cdbab80d002?auto=format&fit=crop&w=900&q=80",
        tags: ["手拍披薩", "熔岩巧克力", "派對套餐"],
        menu: [
          { id: "m1201", name: "超級豪華大披薩（12吋）", category: "主食", price: 550, desc: "雙重起司鋪滿義式臘腸、火腿、洋蔥、青椒與香烤蘑菇", img: "https://images.unsplash.com/photo-1574071318508-1cdbab80d002?auto=format&fit=crop&w=400&q=80" },
          { id: "m1202", name: "雙人派對歡樂餐", category: "套餐", price: 399, desc: "9吋經典披薩＋香烤雞翅4支＋蒜香起司球＋1.25L雪碧", img: "https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?auto=format&fit=crop&w=400&q=80" },
          { id: "m1203", name: "爆漿熔岩巧克力蛋糕", category: "甜點", price: 99, desc: "外酥內熱，切開即流出濃郁苦甜比利時巧克力熔岩", img: "https://images.unsplash.com/photo-1564355808539-22fda35bed7e?auto=format&fit=crop&w=400&q=80" },
          { id: "m1204", name: "雪碧汽水（1.25L 分享瓶）", category: "飲料", price: 50, desc: "清涼暢快檸檬氣泡飲，適合多人共享", img: "https://images.unsplash.com/photo-1622483767028-3f66f32aef97?auto=format&fit=crop&w=400&q=80" }
        ]
      }
    ];

    // ==========================================
    // 3. 工具函式與持久化狀態管理
    // ==========================================
    function escapeHtml(str) {
      return String(str ?? "")
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;")
        .replace(/'/g, "&#39;");
    }

    function formatDateTime(date) {
      const pad = n => String(n).padStart(2, "0");
      return `${date.getFullYear()}-${pad(date.getMonth() + 1)}-${pad(date.getDate())} ${pad(date.getHours())}:${pad(date.getMinutes())}`;
    }

    function buildGoogleMapsEmbedUrl(query) {
      return `https://maps.google.com/maps?q=${encodeURIComponent(query)}&hl=zh-TW&z=16&output=embed`;
    }

    function buildGoogleMapsExternalUrl(query) {
      return `https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(query)}`;
    }

    function getStatusSteps(mode) {
      return mode === "pickup"
        ? ["餐廳已接單", "餐點製作中", "已備妥待取餐", "已完成自取"]
        : ["餐廳已接單", "餐點製作中", "外送員配送中", "已送達"];
    }

    function createDefaultUsers() {
      const yesterday = new Date(Date.now() - 86400000);
      return {
        student01: {
          username: "student01",
          display_name: "王小明",
          birthday: "2004-05-18",
          phone: "0912345678",
          custom_card: null,
          location_enabled: true,
          location_label: "台中市霧峰區中正路800號",
          delivery_address: "台中市霧峰區中正路800號",
          google_email: null,
          invoice_carrier: "/AB12345",
          is_vip: false,
          favorites: ["r2", "r7"],
          cart: [],
          orders: [
            {
              order_id: `ORD-${yesterday.getFullYear()}${String(yesterday.getMonth() + 1).padStart(2, "0")}${String(yesterday.getDate()).padStart(2, "0")}-01`,
              created_at: formatDateTime(yesterday),
              delivery_mode: "delivery",
              delivery_address: "台中市霧峰區中正路800號",
              delivery_address_note: "放管理室",
              payment_label: "貨到付款（現金）",
              invoice_label: "手機條碼載具（/AB12345）",
              status_index: 3,
              status: "已送達",
              items: [
                {
                  restaurant_id: "r2",
                  restaurant_name: "茶語軒手搖專門店",
                  restaurant_category: "手搖飲",
                  item_id: "m201",
                  name: "黑糖珍珠鮮奶茶",
                  category: "飲料",
                  base_price: 70,
                  unit_price: 80,
                  qty: 2,
                  ice: "微冰",
                  sugar: "微糖",
                  addons: ["加黑糖珍珠"],
                  note: ""
                }
              ],
              subtotal: 160,
              delivery_fee: 39,
              service_fee: 15,
              discount: 0,
              total: 214,
              promo_code: ""
            }
          ]
        }
      };
    }

    let USERS = createDefaultUsers();
    let CURRENT_USER_KEY = null; // 預設未登入，右上角顯示「登入」
    let GUEST_CART = [];

    function loadPersistedState() {
      try {
        const rawUsers = localStorage.getItem(STORAGE_USERS_KEY);
        if (rawUsers) {
          const parsed = JSON.parse(rawUsers);
          if (parsed && typeof parsed === "object") {
            USERS = Object.assign(createDefaultUsers(), parsed);
          }
        }
        const savedUserKey = localStorage.getItem(STORAGE_CURRENT_KEY);
        if (savedUserKey && USERS[savedUserKey]) {
          CURRENT_USER_KEY = savedUserKey;
        }
      } catch (e) {
        console.warn("讀取本地狀態失敗，使用預設資料", e);
      }
    }

    function savePersistedState() {
      try {
        localStorage.setItem(STORAGE_USERS_KEY, JSON.stringify(USERS));
        if (CURRENT_USER_KEY) {
          localStorage.setItem(STORAGE_CURRENT_KEY, CURRENT_USER_KEY);
        } else {
          localStorage.removeItem(STORAGE_CURRENT_KEY);
        }
      } catch (e) {
        console.warn("寫入本地狀態失敗", e);
      }
    }

    function isLoggedIn() {
      return Boolean(CURRENT_USER_KEY && USERS[CURRENT_USER_KEY]);
    }

    function getUser() {
      if (isLoggedIn()) return USERS[CURRENT_USER_KEY];
      return {
        username: null,
        display_name: "訪客",
        is_vip: false,
        favorites: [],
        cart: GUEST_CART,
        orders: [],
        google_email: null,
        invoice_carrier: "",
        custom_card: null,
        delivery_address: deliveryAddress
      };
    }

    // 介面狀態變數
    let currentTab = "home";
    let selectedRestCategory = "全部";
    let selectedMealCategory = "全部";
    let searchQuery = "";
    let searchDebounceTimer = null;
    let deliveryMode = "delivery";
    let promoCode = "";
    let selectedPaymentMethod = "cash";
    let selectedSavedCardId = "card_visa";
    let showNewCardForm = false;
    let selectedInvoiceType = "member";
    let invoiceCarrierDraft = "";
    let invoiceDonateCode = "919";
    let invoiceTaxId = "";
    let deliveryAddress = "台中市霧峰區中正路800號";
    let deliveryAddressNote = "";
    let addressModalMode = "checkout";
    let pendingCheckoutData = null;
    let googleOAuthMode = "login";
    let activeRestaurant = null;
    let activeMenuItem = null;
    let customQty = 1;
    let highlightedOrderId = null;
    let autoAdvanceTimer = null;
    let toastTimer = null;
    let lastFocusedBeforeModal = null;
    let regStep = 1;
    let regDraft = { username: "", name: "", birthday: "", phone: "", custom_card: null, location_enabled: false, location_label: "" };

    // ==========================================
    // 4. Modal 捲動鎖定、焦點管理與 Escape 關閉
    // ==========================================
    const MODAL_IDS = ["menu-modal", "custom-modal", "vip-modal", "login-modal", "register-modal", "google-oauth-modal", "address-modal", "checkout-confirm-modal"];

    function isAnyModalOpen() {
      return MODAL_IDS.some(id => !document.getElementById(id).classList.contains("hidden"));
    }

    function updateBodyScrollLock() {
      document.body.style.overflow = isAnyModalOpen() ? "hidden" : "";
    }

    function focusModal(modalId) {
      const el = document.getElementById(modalId);
      if (!el) return;
      const focusable = el.querySelector('input:not([disabled]), button:not([disabled]), select:not([disabled]), [tabindex]:not([tabindex="-1"])');
      if (focusable) setTimeout(() => focusable.focus(), 40);
    }

    function restoreFocusIfAllClosed() {
      if (!isAnyModalOpen() && lastFocusedBeforeModal && typeof lastFocusedBeforeModal.focus === "function") {
        lastFocusedBeforeModal.focus();
        lastFocusedBeforeModal = null;
      }
    }

    document.addEventListener("keydown", (e) => {
      if (e.key !== "Escape") return;
      if (!document.getElementById("checkout-confirm-modal").classList.contains("hidden")) closeCheckoutConfirmModal();
      else if (!document.getElementById("address-modal").classList.contains("hidden")) closeAddressModal();
      else if (!document.getElementById("google-oauth-modal").classList.contains("hidden")) closeGoogleOAuthModal();
      else if (!document.getElementById("register-modal").classList.contains("hidden")) closeRegisterModal();
      else if (!document.getElementById("custom-modal").classList.contains("hidden")) closeCustomModal();
      else if (!document.getElementById("vip-modal").classList.contains("hidden")) closeVipModal();
      else if (!document.getElementById("login-modal").classList.contains("hidden")) closeLoginModal();
      else if (!document.getElementById("menu-modal").classList.contains("hidden")) closeMenuModal();
    });

    // ==========================================
    // 5. 核心商業邏輯：口味推薦與購物車試算
    // ==========================================
    function analyzeUserPreferences(user) {
      const counts = {};
      (user.orders || []).forEach(o => {
        (o.items || []).forEach(item => {
          const cat = item.restaurant_category;
          if (cat) counts[cat] = (counts[cat] || 0) + (item.qty || 1);
        });
      });

      const entries = Object.entries(counts).sort((a, b) => b[1] - a[1]);
      if (!entries.length) {
        const topList = [...RESTAURANTS].sort((a, b) => b.rating - a.rating).slice(0, 8);
        return {
          has_history: false,
          top_taste: null,
          taste_stats: {},
          reason: "為您精選周邊高評分人氣餐廳（完成第一筆訂單後將自動啟動 AI 口味偏好推薦）",
          restaurants: topList
        };
      }

      const [topTaste, topCount] = entries[0];
      const matched = RESTAURANTS.filter(r => r.category === topTaste);
      const others = RESTAURANTS.filter(r => r.category !== topTaste).sort((a, b) => b.rating - a.rating);
      const recommended = [...matched, ...others].slice(0, 8);

      return {
        has_history: true,
        top_taste: topTaste,
        taste_stats: counts,
        reason: `根據歷史點餐分析，您最偏愛「${topTaste}」（累計 ${topCount} 份），優先為您排序相關愛店`,
        restaurants: recommended
      };
    }

    function calculateCartSummary(user, mode, codeInput) {
      const cart = user.cart || [];
      const subtotal = cart.reduce((sum, i) => sum + i.unit_price * i.qty, 0);
      if (subtotal === 0) {
        return { subtotal: 0, delivery_fee: 0, service_fee: 0, discount: 0, total: 0, promo_msg: "", promo_valid: false };
      }

      const isVip = Boolean(user.is_vip);
      const delivery_fee = (mode === "pickup" || isVip) ? 0 : PRICING.DELIVERY_FEE;
      const service_fee = isVip ? 0 : PRICING.SERVICE_FEE;

      let discount = 0;
      let promo_msg = "";
      let promo_valid = false;
      const code = (codeInput || "").trim().toUpperCase();

      if (code) {
        if (!isVip) {
          promo_msg = "此優惠碼僅限 FoodOrder One 付費會員使用，請先升級或清除優惠碼";
        } else if (PRICING.VIP_PROMO_CODES[code]) {
          const rule = PRICING.VIP_PROMO_CODES[code];
          discount = rule.type === "percent" ? Math.round(subtotal * rule.value) : Math.min(subtotal, rule.value);
          promo_msg = `已套用 ${code}（${rule.label}），折抵 $${discount}`;
          promo_valid = true;
        } else {
          promo_msg = "無效的優惠碼（可試用 PRO85 或 VIP50）";
        }
      }

      const total = Math.max(0, subtotal + delivery_fee + service_fee - discount);
      return { subtotal, delivery_fee, service_fee, discount, total, promo_msg, promo_valid };
    }

    // ==========================================
    // 6. Toast 通知與分頁切換
    // ==========================================
    function showToast(msg, actionText = null, actionFn = null) {
      const toast = document.getElementById("toast");
      const msgEl = document.getElementById("toast-msg");
      const btnEl = document.getElementById("toast-action-btn");
      msgEl.textContent = msg;

      if (actionText && typeof actionFn === "function") {
        btnEl.textContent = actionText;
        btnEl.classList.remove("hidden");
        btnEl.onclick = () => {
          actionFn();
          toast.classList.add("hidden");
        };
      } else {
        btnEl.classList.add("hidden");
        btnEl.onclick = null;
      }

      toast.classList.remove("hidden");
      clearTimeout(toastTimer);
      toastTimer = setTimeout(() => toast.classList.add("hidden"), actionText ? 4200 : 2600);
    }

    function switchTab(tab, shouldScrollTop = true) {
      currentTab = tab;
      ["home", "favorites", "orders", "cart"].forEach(t => {
        document.getElementById(`view-${t}`).classList.toggle("hidden", t !== tab);
        const btn = document.getElementById(`tab-${t}`);
        if (t === tab) {
          btn.classList.add("border-neutral-950", "text-neutral-950");
          btn.classList.remove("border-transparent", "text-neutral-500");
        } else {
          btn.classList.remove("border-neutral-950", "text-neutral-950");
          btn.classList.add("border-transparent", "text-neutral-500");
        }
      });
      renderCurrentView();
      if (shouldScrollTop) window.scrollTo({ top: 0, behavior: "smooth" });
    }

    function renderCurrentView() {
      renderHeader();
      if (currentTab === "home") renderHome();
      else if (currentTab === "favorites") renderFavorites();
      else if (currentTab === "orders") renderOrders();
      else if (currentTab === "cart") renderCart();
    }

    // ==========================================
    // 7. 頂部導覽列與各分頁渲染
    // ==========================================
    function renderHeader() {
      const u = getUser();
      const loggedIn = isLoggedIn();
      const totalQty = (u.cart || []).reduce((s, i) => s + i.qty, 0);
      document.getElementById("cart-count-badge").textContent = totalQty;

      // 使用者名稱與頭像
      const nameLabel = document.getElementById("user-name-label");
      const avatarEl = document.getElementById("header-user-avatar");
      if (loggedIn) {
        nameLabel.textContent = u.display_name;
        if (u.google_email) {
          avatarEl.className = "w-5 h-5 rounded-full bg-blue-600 text-white flex items-center justify-center text-[10px] font-bold";
          avatarEl.textContent = (u.display_name || "G").charAt(0).toUpperCase();
        } else {
          avatarEl.className = "w-5 h-5 rounded-full bg-neutral-900 text-white flex items-center justify-center text-[10px] font-bold";
          avatarEl.textContent = (u.display_name || "U").charAt(0).toUpperCase();
        }
      } else {
        nameLabel.textContent = "登入";
        avatarEl.className = "w-5 h-5 rounded-full bg-neutral-300 text-neutral-700 flex items-center justify-center";
        avatarEl.innerHTML = `<svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>`;
      }

      // 會員徽章按鈕
      const vipDesktop = document.getElementById("vip-badge-btn");
      const vipMobile = document.getElementById("vip-badge-mobile");
      const heroVipBtn = document.getElementById("hero-vip-btn");
      if (loggedIn && u.is_vip) {
        vipDesktop.textContent = "One 會員";
        vipDesktop.className = "hidden sm:inline-flex items-center gap-1.5 px-3.5 py-2 rounded-full text-xs font-extrabold bg-[#06C167] text-neutral-950 hover:bg-[#05a858] transition cursor-pointer";
        vipMobile.textContent = "One 會員";
        vipMobile.className = "px-3 py-1.5 rounded-full text-xs font-extrabold bg-[#06C167] text-neutral-950 shrink-0";
        if (heroVipBtn) heroVipBtn.textContent = "管理我的 One 會員";
      } else {
        vipDesktop.textContent = "升級 One";
        vipDesktop.className = "hidden sm:inline-flex items-center gap-1.5 px-3.5 py-2 rounded-full text-xs font-bold bg-amber-100 text-amber-900 hover:bg-amber-200 transition cursor-pointer";
        vipMobile.textContent = "升級 One";
        vipMobile.className = "px-3 py-1.5 rounded-full text-xs font-bold bg-amber-100 text-amber-900 shrink-0";
        if (heroVipBtn) heroVipBtn.textContent = "立即體驗 FoodOrder One";
      }

      // 外送 / 自取切換按鈕
      document.getElementById("mode-delivery").className = deliveryMode === "delivery"
        ? "px-3.5 py-1.5 rounded-full bg-white text-neutral-950 shadow-sm transition cursor-pointer"
        : "px-3.5 py-1.5 rounded-full text-neutral-600 hover:text-neutral-950 transition cursor-pointer";
      document.getElementById("mode-pickup").className = deliveryMode === "pickup"
        ? "px-3.5 py-1.5 rounded-full bg-white text-neutral-950 shadow-sm transition cursor-pointer"
        : "px-3.5 py-1.5 rounded-full text-neutral-600 hover:text-neutral-950 transition cursor-pointer";

      // 頂部地址顯示
      const activeAddr = (loggedIn && u.delivery_address)
        ? u.delivery_address
        : (loggedIn && u.location_enabled && u.location_label)
          ? u.location_label
          : deliveryAddress;
      const locDesktop = document.getElementById("header-location-label");
      const locMobile = document.getElementById("mobile-location-label");
      if (locDesktop) locDesktop.textContent = `${activeAddr} • ${deliveryMode === "pickup" ? "來店自取" : "立即送達"}`;
      if (locMobile) locMobile.textContent = activeAddr;
    }

    function heartSvg(isFav) {
      return isFav
        ? `<svg class="w-4 h-4 text-red-500 fill-red-500" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>`
        : `<svg class="w-4 h-4 text-neutral-700" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"/></svg>`;
    }

    // 精巧版橫排推薦卡片（一次顯示 4 家）
    function compactRecCardHTML(r) {
      const isFav = isLoggedIn() && getUser().favorites.includes(r.id);
      const timeLabel = deliveryMode === "pickup" ? `約 ${r.pickup_time} 取餐` : r.delivery_time;
      return `
        <div onclick="openMenuModal('${r.id}')" class="w-[240px] sm:w-[230px] lg:w-[calc(25%-12px)] shrink-0 snap-start group bg-white rounded-2xl border border-neutral-200/80 hover:border-neutral-300 hover:shadow-md transition overflow-hidden cursor-pointer flex flex-col">
          <div class="relative aspect-[16/10] bg-neutral-100 overflow-hidden">
            <img src="${r.cover}" alt="${escapeHtml(r.name)}" onerror="handleImgError(this)" class="w-full h-full object-cover group-hover:scale-105 transition duration-300" />
            <button type="button" data-fav-btn="${r.id}" onclick="event.stopPropagation(); toggleFavorite('${r.id}')" aria-label="${isFav ? '取消收藏' : '加入收藏'}"
              class="absolute top-2.5 right-2.5 w-7 h-7 rounded-full bg-white/90 hover:bg-white shadow flex items-center justify-center transition cursor-pointer">
              ${heartSvg(isFav)}
            </button>
            <span class="absolute bottom-2 left-2 px-2 py-0.5 rounded-full bg-white/95 text-[10px] font-bold text-neutral-900 shadow-sm">
              ★ ${r.rating}
            </span>
          </div>
          <div class="p-3 space-y-1 flex-1 flex flex-col justify-between">
            <h3 class="font-bold text-sm text-neutral-950 truncate group-hover:text-[#059652] transition">${escapeHtml(r.name)}</h3>
            <div class="flex items-center justify-between text-[11px] text-neutral-500">
              <span>${escapeHtml(r.category)}</span>
              <span>${escapeHtml(timeLabel)}</span>
            </div>
          </div>
        </div>
      `;
    }

    // 標準版附近熱門餐廳大卡片（一排 3 家）
    function standardRestaurantCardHTML(r) {
      const u = getUser();
      const isFav = isLoggedIn() && u.favorites.includes(r.id);
      const timeLabel = deliveryMode === "pickup" ? `約 ${r.pickup_time} 可取餐` : r.delivery_time;
      const feeText = deliveryMode === "pickup"
        ? "自取免運費"
        : (u.is_vip ? "One 會員 $0 外送費" : `$${PRICING.DELIVERY_FEE} 外送費`);

      return `
        <article onclick="openMenuModal('${r.id}')" class="group bg-white rounded-2xl border border-neutral-200/80 hover:border-neutral-300 hover:shadow-lg transition duration-200 overflow-hidden cursor-pointer flex flex-col">
          <div class="relative aspect-[16/9] bg-neutral-100 overflow-hidden">
            <img src="${r.cover}" alt="${escapeHtml(r.name)}" onerror="handleImgError(this)" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" />
            <button type="button" data-fav-btn="${r.id}" onclick="event.stopPropagation(); toggleFavorite('${r.id}')" aria-label="${isFav ? '取消收藏' : '加入收藏'}"
              class="absolute top-3 right-3 w-8 h-8 rounded-full bg-white/90 hover:bg-white shadow-md flex items-center justify-center transition cursor-pointer">
              ${heartSvg(isFav)}
            </button>
            <div class="absolute bottom-3 left-3 flex items-center gap-1.5">
              <span class="px-2.5 py-1 rounded-full bg-white/95 text-xs font-extrabold text-neutral-950 shadow-sm">★ ${r.rating} <span class="font-medium text-neutral-500">(${r.reviews})</span></span>
            </div>
          </div>
          <div class="p-4 flex-1 flex flex-col justify-between space-y-2.5">
            <div>
              <div class="flex items-start justify-between gap-2">
                <h3 class="font-extrabold text-base text-neutral-950 group-hover:text-[#059652] transition leading-snug">${escapeHtml(r.name)}</h3>
              </div>
              <p class="text-xs text-neutral-500 mt-1">${escapeHtml(r.category)} • ${escapeHtml(timeLabel)} • ${escapeHtml(r.distance)}</p>
              <p class="text-[11px] text-neutral-400 mt-0.5 truncate">${escapeHtml(r.address)}</p>
            </div>
            <div class="pt-2 border-t border-neutral-100 flex items-center justify-between text-xs">
              <span class="font-semibold ${deliveryMode === 'pickup' || u.is_vip ? 'text-[#059652]' : 'text-neutral-600'}">${feeText}</span>
              <span class="text-neutral-400">低消 $${r.min_order}</span>
            </div>
          </div>
        </article>
      `;
    }

    function scrollRecommendations(dir) {
      const container = document.getElementById("recommended-carousel");
      if (!container) return;
      const step = Math.max(260, container.clientWidth * 0.75);
      container.scrollBy({ left: dir * step, behavior: "smooth" });
    }

    function renderHome() {
      // 分類按鈕
      document.getElementById("restaurant-category-tabs").innerHTML = REST_CATEGORIES.map(c => `
        <button type="button" onclick="selectRestCategory('${c}')"
          class="px-4 py-2 rounded-full text-xs font-bold whitespace-nowrap transition cursor-pointer ${selectedRestCategory === c ? 'bg-neutral-950 text-white shadow-sm' : 'bg-neutral-100 text-neutral-700 hover:bg-neutral-200'}">
          ${c}
        </button>
      `).join("");

      // AI 口味推薦橫排 4 卡輪播
      const rec = analyzeUserPreferences(getUser());
      document.getElementById("rec-reason").textContent = rec.reason;
      const statsEntries = Object.entries(rec.taste_stats);
      document.getElementById("taste-stats-pills").innerHTML = statsEntries.length
        ? statsEntries.map(([k, v]) => `<span class="px-2.5 py-1 bg-neutral-100 rounded-full text-neutral-700 font-semibold">${escapeHtml(k)} ${v}份</span>`).join("")
        : `<span class="px-2.5 py-1 bg-neutral-100 rounded-full text-neutral-500 font-medium">完成第一筆訂單後，這裡會顯示您的口味分析</span>`;

      document.getElementById("recommended-carousel").innerHTML = rec.restaurants.map(compactRecCardHTML).join("");

      // 搜尋與分類過濾（含餐點描述 m.desc 匹配）
      const q = searchQuery.trim().toLowerCase();
      const filtered = RESTAURANTS.filter(r => {
        const matchCat = selectedRestCategory === "全部" || r.category === selectedRestCategory;
        const matchQuery = !q ||
          r.name.toLowerCase().includes(q) ||
          r.category.toLowerCase().includes(q) ||
          r.address.toLowerCase().includes(q) ||
          r.tags.some(t => t.toLowerCase().includes(q)) ||
          r.menu.some(m => m.name.toLowerCase().includes(q) || m.desc.toLowerCase().includes(q));
        return matchCat && matchQuery;
      });

      document.getElementById("restaurants-count-label").textContent = `共 ${filtered.length} 家餐廳`;
      document.getElementById("restaurants-grid").innerHTML = filtered.length
        ? filtered.map(standardRestaurantCardHTML).join("")
        : `<div class="col-span-full py-12 text-center bg-neutral-50 rounded-2xl border border-neutral-200 text-sm text-neutral-500">找不到符合「${escapeHtml(searchQuery)}」的餐廳或餐點，試試其他關鍵字吧。</div>`;
    }

    function selectRestCategory(cat) {
      selectedRestCategory = cat;
      renderHome();
    }

    function handleSearchInput(val) {
      searchQuery = val;
      const d = document.getElementById("search-input-desktop");
      const m = document.getElementById("search-input-mobile");
      if (d && d.value !== val) d.value = val;
      if (m && m.value !== val) m.value = val;

      clearTimeout(searchDebounceTimer);
      searchDebounceTimer = setTimeout(() => {
        if (searchQuery.trim() && selectedRestCategory !== "全部") {
          selectedRestCategory = "全部";
        }
        if (currentTab !== "home") {
          switchTab("home", false);
        } else {
          renderHome();
        }
      }, 180);
    }

    function renderFavorites() {
      const grid = document.getElementById("favorites-grid");
      if (!isLoggedIn()) {
        grid.innerHTML = `
          <div class="col-span-full py-14 text-center bg-neutral-50 rounded-2xl border border-neutral-200 space-y-3">
            <p class="text-sm font-semibold text-neutral-700">登入帳號即可查看與同步您的愛店口袋名單</p>
            <button type="button" onclick="openLoginModal()" class="px-5 py-2.5 bg-neutral-950 text-white text-xs font-bold rounded-full cursor-pointer">前往登入</button>
          </div>`;
        return;
      }
      const favs = RESTAURANTS.filter(r => getUser().favorites.includes(r.id));
      grid.innerHTML = favs.length
        ? favs.map(standardRestaurantCardHTML).join("")
        : `<div class="col-span-full py-14 text-center bg-neutral-50 rounded-2xl border border-neutral-200 text-sm text-neutral-500">口袋名單目前是空的，點擊餐廳右上角的愛心即可收藏愛店。</div>`;
    }

    function renderOrders() {
      const list = document.getElementById("orders-list");
      if (!isLoggedIn()) {
        list.innerHTML = `
          <div class="py-14 text-center bg-neutral-50 rounded-2xl border border-neutral-200 space-y-3">
            <p class="text-sm font-semibold text-neutral-700">登入後即可檢視歷史訂單、即時追蹤狀態與一鍵再次點購</p>
            <button type="button" onclick="openLoginModal()" class="px-5 py-2.5 bg-neutral-950 text-white text-xs font-bold rounded-full cursor-pointer">前往登入</button>
          </div>`;
        return;
      }

      const orders = getUser().orders || [];
      if (!orders.length) {
        list.innerHTML = `<div class="py-14 text-center bg-neutral-50 rounded-2xl border border-neutral-200 text-sm text-neutral-500">尚無歷史訂單紀錄，快去挑選喜歡的美食吧！</div>`;
        return;
      }

      list.innerHTML = orders.map(o => {
        const steps = getStatusSteps(o.delivery_mode);
        const isHighlighted = highlightedOrderId === o.order_id;
        return `
          <div class="bg-white p-5 rounded-2xl border ${isHighlighted ? 'border-[#06C167] ring-2 ring-[#06C167]/40' : 'border-neutral-200'} shadow-sm space-y-4 transition">
            <div class="flex flex-wrap items-center justify-between gap-2 border-b border-neutral-100 pb-3">
              <div class="flex flex-wrap items-center gap-2">
                <span class="font-extrabold text-sm text-neutral-950">${escapeHtml(o.order_id)}</span>
                <span class="text-xs text-neutral-400">${escapeHtml(o.created_at)}</span>
                <span class="text-[11px] font-bold px-2.5 py-0.5 rounded-full bg-neutral-100 text-neutral-700">${o.delivery_mode === "pickup" ? "來店自取" : "外送服務"}</span>
                ${o.payment_label ? `<span class="text-[11px] font-semibold px-2.5 py-0.5 rounded-full bg-blue-50 text-blue-700">${escapeHtml(o.payment_label)}</span>` : ""}
                ${o.invoice_label ? `<span class="text-[11px] font-semibold px-2.5 py-0.5 rounded-full bg-emerald-50 text-[#059652]">${escapeHtml(o.invoice_label)}</span>` : ""}
              </div>
              <div class="flex items-center gap-2">
                ${o.status_index < 3 ? `<button type="button" onclick="advanceOrder('${o.order_id}')" class="px-3 py-1.5 text-xs font-semibold bg-neutral-100 hover:bg-neutral-200 text-neutral-800 rounded-lg cursor-pointer">模擬推進進度</button>` : ""}
                <button type="button" onclick="reorder('${o.order_id}')" class="px-3.5 py-1.5 text-xs font-bold bg-neutral-950 hover:bg-neutral-800 text-white rounded-lg cursor-pointer">再次點購</button>
              </div>
            </div>

            <!-- 狀態進度條 -->
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-2 text-center text-xs">
              ${steps.map((st, idx) => `
                <div class="py-2 px-2 rounded-xl font-semibold ${idx <= o.status_index ? 'bg-emerald-50 text-[#059652] border border-emerald-200' : 'bg-neutral-50 text-neutral-400 border border-neutral-100'}">
                  ${idx <= o.status_index ? '✓ ' : ''}${st}
                </div>
              `).join("")}
            </div>

            <!-- 餐點明細 -->
            <div class="space-y-1.5 text-xs">
              ${o.items.map(i => `
                <div class="flex justify-between gap-2 text-neutral-700">
                  <span>
                    <b class="text-neutral-900">[${escapeHtml(i.restaurant_name)}]</b> ${escapeHtml(i.name)} × ${i.qty}
                    <span class="text-neutral-400">(${escapeHtml(i.ice)}/${escapeHtml(i.sugar)}${i.addons && i.addons.length ? '/+' + escapeHtml(i.addons.join(',')) : ''}${i.note ? '/備註:' + escapeHtml(i.note) : ''})</span>
                  </span>
                  <span class="font-bold text-neutral-900 shrink-0">$${i.unit_price * i.qty}</span>
                </div>
              `).join("")}
            </div>

            <!-- 費用總結與配送地址 -->
            <div class="flex flex-wrap justify-between items-center pt-3 border-t border-neutral-100 text-xs text-neutral-500 gap-2">
              <div class="space-y-1">
                ${o.delivery_address ? `
                  <div class="flex items-center gap-1.5 text-neutral-700">
                    <span>${o.delivery_mode === "pickup" ? "自取門市" : "送達地址"}：${escapeHtml(o.delivery_address)}${o.delivery_address_note ? `（${escapeHtml(o.delivery_address_note)}）` : ""}</span>
                    <a href="${buildGoogleMapsExternalUrl(o.delivery_address)}" target="_blank" rel="noopener noreferrer" class="text-[#059652] hover:underline font-semibold shrink-0">地圖 ↗</a>
                  </div>
                ` : ""}
                <span>外送費 $${o.delivery_fee} • 服務費 $${o.service_fee}${o.discount ? ` • 會員折扣 -$${o.discount}` : ""}</span>
              </div>
              <span class="font-extrabold text-base text-neutral-950">實付總額 $${o.total}</span>
            </div>
          </div>
        `;
      }).join("");
    }

    function renderCart() {
      const u = getUser();
      const cart = u.cart || [];
      const sum = calculateCartSummary(u, deliveryMode, promoCode);

      // 按餐廳分組
      const grouped = {};
      cart.forEach(item => {
        if (!grouped[item.restaurant_id]) {
          grouped[item.restaurant_id] = { name: item.restaurant_name, items: [] };
        }
        grouped[item.restaurant_id].items.push(item);
      });
      const groupKeys = Object.keys(grouped);

      const crossNotice = document.getElementById("cross-store-notice");
      if (groupKeys.length > 1) {
        crossNotice.textContent = `提醒：您的購物車包含 ${groupKeys.length} 家不同餐廳的餐點，外送員將分別取餐（本次示範合併計算一筆運費）。`;
        crossNotice.classList.remove("hidden");
      } else {
        crossNotice.classList.add("hidden");
      }

      const listEl = document.getElementById("cart-items-list");
      document.getElementById("clear-cart-btn").classList.toggle("hidden", cart.length === 0);

      if (!cart.length) {
        listEl.innerHTML = `
          <div class="py-14 text-center bg-neutral-50 rounded-2xl border border-neutral-200 space-y-3">
            <p class="text-sm font-semibold text-neutral-600">您的購物車目前是空的</p>
            <button type="button" onclick="switchTab('home')" class="px-5 py-2.5 bg-neutral-950 text-white text-xs font-bold rounded-full cursor-pointer">去探索附近美食</button>
          </div>`;
      } else {
        listEl.innerHTML = groupKeys.map(rid => {
          const g = grouped[rid];
          return `
            <div class="bg-white border border-neutral-200 rounded-2xl overflow-hidden">
              <div class="px-4 py-3 bg-neutral-50 border-b border-neutral-100 flex items-center justify-between">
                <span class="font-extrabold text-sm text-neutral-950">${escapeHtml(g.name)}</span>
                <button type="button" onclick="openMenuModal('${rid}')" class="text-xs font-bold text-[#059652] hover:underline cursor-pointer">+ 繼續加點</button>
              </div>
              <div class="divide-y divide-neutral-100">
                ${g.items.map(i => `
                  <div class="p-4 flex items-start justify-between gap-3">
                    <div class="space-y-0.5 min-w-0">
                      <p class="font-bold text-sm text-neutral-950">${escapeHtml(i.name)} × ${i.qty}</p>
                      <p class="text-xs text-neutral-500">
                        ${escapeHtml(i.ice)} / ${escapeHtml(i.sugar)}${i.addons && i.addons.length ? ' / +' + escapeHtml(i.addons.join('、')) : ''}
                      </p>
                      ${i.note ? `<p class="text-[11px] text-neutral-400">備註：${escapeHtml(i.note)}</p>` : ""}
                    </div>
                    <div class="flex items-center gap-3 shrink-0">
                      <span class="font-bold text-sm text-neutral-950">$${i.unit_price * i.qty}</span>
                      <button type="button" onclick="removeCartItem('${i.cart_item_id}')" class="text-xs font-semibold text-neutral-400 hover:text-red-600 cursor-pointer">移除</button>
                    </div>
                  </div>
                `).join("")}
              </div>
            </div>
          `;
        }).join("");
      }

      // 會員提示橫幅
      const banner = document.getElementById("vip-promo-banner");
      if (isLoggedIn() && u.is_vip) {
        banner.className = "p-3.5 rounded-xl text-xs leading-relaxed bg-emerald-50 border border-emerald-200 text-emerald-950";
        banner.innerHTML = `<b>FoodOrder One 付費會員生效中</b>：已自動免除 $39 外送費與 $15 平台服務費，並可套用折扣碼 <b>PRO85</b> 或 <b>VIP50</b>。`;
      } else {
        banner.className = "p-3.5 rounded-xl text-xs leading-relaxed bg-white border border-neutral-200 text-neutral-600";
        banner.innerHTML = `目前為 <b>一般會員</b>（外送費 $${PRICING.DELIVERY_FEE}、服務費 $${PRICING.SERVICE_FEE}）。<button type="button" onclick="openVipModal()" class="text-[#059652] font-bold hover:underline ml-1 cursor-pointer">立即升級免運</button>`;
      }

      // 空購物車時禁用優惠碼與結帳按鈕
      const isEmpty = cart.length === 0;
      const promoInput = document.getElementById("promo-input");
      const applyBtn = document.getElementById("apply-promo-btn");
      const checkoutBtn = document.getElementById("checkout-btn");
      promoInput.disabled = isEmpty;
      applyBtn.disabled = isEmpty;
      checkoutBtn.disabled = isEmpty;
      if (promoInput.value !== promoCode) promoInput.value = promoCode;

      const pMsg = document.getElementById("promo-msg");
      if (!sum.promo_msg) {
        pMsg.textContent = isEmpty ? "請先加入餐點後再輸入優惠碼" : "";
        pMsg.className = "text-xs min-h-[16px] text-neutral-400";
      } else {
        pMsg.textContent = sum.promo_msg;
        pMsg.className = `text-xs min-h-[16px] font-semibold ${sum.promo_valid ? "text-[#059652]" : "text-red-600"}`;
      }

      // 同步付款方式與載具 UI
      renderPaymentUI();
      renderInvoiceUI();

      // 費用明細
      document.getElementById("sum-mode-label").textContent = deliveryMode === "pickup" ? "來店自取・免運費" : (u.is_vip ? "One 會員・免運費" : "外送");
      document.getElementById("sum-subtotal").textContent = `$${sum.subtotal}`;
      document.getElementById("sum-delivery").textContent = `$${sum.delivery_fee}`;
      document.getElementById("sum-service").textContent = `$${sum.service_fee}`;
      document.getElementById("sum-discount").textContent = `-$${sum.discount}`;
      document.getElementById("sum-total").textContent = `$${sum.total}`;
    }

    // ==========================================
    // 8. 餐廳菜單 Modal 與 Google 地圖展開
    // ==========================================
    function openMenuModal(rid) {
      const r = RESTAURANTS.find(x => x.id === rid);
      if (!r) return;
      lastFocusedBeforeModal = document.activeElement;
      activeRestaurant = r;
      selectedMealCategory = "全部";
      renderMenuModal(true);
      document.getElementById("menu-modal").classList.remove("hidden");
      updateBodyScrollLock();
      focusModal("menu-modal");
    }

    function closeMenuModal() {
      activeRestaurant = null;
      document.getElementById("menu-modal").classList.add("hidden");
      updateBodyScrollLock();
      restoreFocusIfAllClosed();
    }

    function renderMenuModal(resetScroll = false) {
      if (!activeRestaurant) return;
      const r = activeRestaurant;
      const listEl = document.getElementById("modal-menu-list");
      const prevScroll = resetScroll ? 0 : listEl.scrollTop;

      const coverEl = document.getElementById("modal-rest-cover");
      delete coverEl.dataset.fallbackApplied;
      coverEl.onerror = function() { handleImgError(this); };
      coverEl.src = r.cover;

      document.getElementById("modal-rest-name").textContent = r.name;
      const timeLabel = deliveryMode === "pickup" ? `自取約 ${r.pickup_time}` : `外送約 ${r.delivery_time}`;
      document.getElementById("modal-rest-meta").textContent = `${r.category} • ★ ${r.rating} (${r.reviews}) • ${timeLabel} • 營業 ${r.hours} • 低消 $${r.min_order}`;

      const noticeEl = document.getElementById("modal-rest-notice");
      if (r.notice) {
        noticeEl.textContent = `餐廳公告：${r.notice}`;
        noticeEl.classList.remove("hidden");
      } else {
        noticeEl.classList.add("hidden");
      }

      // 更新餐廳地址與 Google 地圖連結
      const addrText = r.address || "台中市霧峰區中正路";
      document.getElementById("modal-rest-address").textContent = addrText;
      document.getElementById("modal-rest-map-link").href = buildGoogleMapsExternalUrl(`${r.name} ${addrText}`);
      if (resetScroll) {
        document.getElementById("modal-rest-map-wrap").classList.add("hidden");
        document.getElementById("toggle-rest-map-btn").textContent = "查看 Google 地圖";
      }

      document.getElementById("meal-category-tabs").innerHTML = MEAL_CATEGORIES.map(c => `
        <button type="button" onclick="selectedMealCategory='${c}'; renderMenuModal(true)"
          class="px-3.5 py-1.5 rounded-full text-xs font-bold transition cursor-pointer shrink-0 ${selectedMealCategory === c ? 'bg-neutral-950 text-white' : 'bg-neutral-100 text-neutral-600 hover:bg-neutral-200'}">
          ${c}
        </button>
      `).join("");

      const items = r.menu.filter(m => selectedMealCategory === "全部" || m.category === selectedMealCategory);
      listEl.innerHTML = items.length
        ? items.map(m => `
          <div onclick="openCustomModal('${m.id}')" class="bg-white p-3.5 rounded-xl border border-neutral-200 hover:border-neutral-400 hover:shadow-sm transition flex justify-between gap-3 cursor-pointer">
            <div class="flex flex-col justify-between min-w-0">
              <div>
                <div class="flex items-center gap-1.5">
                  <h4 class="font-bold text-sm text-neutral-950 truncate">${escapeHtml(m.name)}</h4>
                </div>
                <p class="text-xs text-neutral-500 mt-1 line-clamp-2">${escapeHtml(m.desc)}</p>
              </div>
              <div class="flex items-center gap-2 mt-2">
                <span class="font-extrabold text-sm text-neutral-950">$${m.price}</span>
                <span class="text-[10px] px-2 py-0.5 rounded bg-neutral-100 text-neutral-600 font-semibold">${escapeHtml(m.category)}</span>
              </div>
            </div>
            <div class="relative w-24 h-24 rounded-xl overflow-hidden bg-neutral-100 shrink-0">
              <img src="${m.img}" alt="${escapeHtml(m.name)}" onerror="handleImgError(this)" class="w-full h-full object-cover" />
              <span class="absolute bottom-1.5 right-1.5 w-7 h-7 rounded-full bg-white shadow text-neutral-950 font-black text-base flex items-center justify-center">+</span>
            </div>
          </div>
        `).join("")
        : `<p class="col-span-full text-center text-neutral-400 py-8 text-sm">此分類目前無餐點。</p>`;

      listEl.scrollTop = prevScroll;
    }

    function toggleRestaurantMap() {
      if (!activeRestaurant) return;
      const wrap = document.getElementById("modal-rest-map-wrap");
      const btn = document.getElementById("toggle-rest-map-btn");
      const iframe = document.getElementById("modal-rest-map-iframe");
      const isHidden = wrap.classList.contains("hidden");

      if (isHidden) {
        iframe.src = buildGoogleMapsEmbedUrl(activeRestaurant.address || activeRestaurant.name);
        wrap.classList.remove("hidden");
        btn.textContent = "隱藏地圖";
      } else {
        wrap.classList.add("hidden");
        btn.textContent = "查看 Google 地圖";
      }
    }

    // ==========================================
    // 9. 餐點客製化 Modal
    // ==========================================
    function openCustomModal(mid) {
      if (!activeRestaurant) return;
      const item = activeRestaurant.menu.find(m => m.id === mid);
      if (!item) return;

      activeMenuItem = item;
      customQty = 1;

      const imgEl = document.getElementById("custom-item-img");
      delete imgEl.dataset.fallbackApplied;
      imgEl.onerror = function() { handleImgError(this); };
      imgEl.src = item.img;

      document.getElementById("custom-item-name").textContent = item.name;
      document.getElementById("custom-item-desc").textContent = item.desc;
      document.getElementById("custom-item-price").textContent = `基本售價 $${item.price}`;
      document.getElementById("custom-note").value = "";
      document.getElementById("custom-qty-display").textContent = "1";

      // 非飲料自動禁用冰塊與甜度
      const isDrink = item.category === "飲料" || activeRestaurant.category === "手搖飲";
      const iceSel = document.getElementById("custom-ice");
      const sugarSel = document.getElementById("custom-sugar");
      const drinkHint = document.getElementById("custom-drink-hint");
      if (isDrink) {
        iceSel.disabled = false;
        sugarSel.disabled = false;
        iceSel.value = "少冰";
        sugarSel.value = "微糖";
        drinkHint.classList.add("hidden");
      } else {
        iceSel.value = "熱飲／不適用";
        sugarSel.value = "無糖／不適用";
        iceSel.disabled = true;
        sugarSel.disabled = true;
        drinkHint.classList.remove("hidden");
      }

      // 依餐廳分類渲染配料
      const addonsMap = CATEGORY_ADDONS[activeRestaurant.category] || CATEGORY_ADDONS["速食"];
      document.getElementById("custom-addons").innerHTML = Object.entries(addonsMap).map(([name, price]) => `
        <label class="flex items-center justify-between gap-2 p-2.5 border border-neutral-200 rounded-xl cursor-pointer hover:bg-neutral-50">
          <span class="flex items-center gap-2">
            <input type="checkbox" value="${escapeHtml(name)}" data-price="${price}" onchange="updateCustomModalTotal()" class="addon-checkbox accent-neutral-950" />
            <span class="font-medium text-neutral-800">${escapeHtml(name)}</span>
          </span>
          <span class="text-neutral-500 font-semibold">+$${price}</span>
        </label>
      `).join("");

      updateCustomModalTotal();
      document.getElementById("custom-modal").classList.remove("hidden");
      updateBodyScrollLock();
      focusModal("custom-modal");
    }

    function closeCustomModal() {
      activeMenuItem = null;
      document.getElementById("custom-modal").classList.add("hidden");
      updateBodyScrollLock();
    }

    function adjustCustomQty(delta) {
      customQty = Math.max(1, customQty + delta);
      document.getElementById("custom-qty-display").textContent = String(customQty);
      updateCustomModalTotal();
    }

    function updateCustomModalTotal() {
      if (!activeMenuItem) return;
      const addonCost = Array.from(document.querySelectorAll(".addon-checkbox:checked"))
        .reduce((s, cb) => s + Number(cb.dataset.price || 0), 0);
      const total = (activeMenuItem.price + addonCost) * customQty;
      document.getElementById("custom-btn-total").textContent = `$${total}`;
    }

    function confirmAddToCart() {
      if (!activeRestaurant || !activeMenuItem) return;
      const checked = Array.from(document.querySelectorAll(".addon-checkbox:checked"));
      const addons = checked.map(cb => cb.value).sort();
      const addonCost = checked.reduce((s, cb) => s + Number(cb.dataset.price || 0), 0);
      const ice = document.getElementById("custom-ice").value;
      const sugar = document.getElementById("custom-sugar").value;
      const note = document.getElementById("custom-note").value.trim();

      const cartItem = {
        cart_item_id: "ci_" + Date.now() + "_" + Math.random().toString(36).slice(2, 6),
        restaurant_id: activeRestaurant.id,
        restaurant_name: activeRestaurant.name,
        restaurant_category: activeRestaurant.category,
        item_id: activeMenuItem.id,
        name: activeMenuItem.name,
        category: activeMenuItem.category,
        base_price: activeMenuItem.price,
        unit_price: activeMenuItem.price + addonCost,
        qty: customQty,
        ice,
        sugar,
        addons,
        note
      };

      const targetCart = isLoggedIn() ? getUser().cart : GUEST_CART;
      mergeItemIntoCart(targetCart, cartItem);
      if (isLoggedIn()) savePersistedState();

      const addedName = activeMenuItem.name;
      closeCustomModal();
      renderHeader();
      if (currentTab === "cart") renderCart();
      showToast(`已加入購物車：${addedName} × ${customQty}`);
    }

    function mergeItemIntoCart(cart, newItem) {
      const sig = `${newItem.item_id}|${newItem.ice}|${newItem.sugar}|${(newItem.addons || []).join(",")}|${newItem.note || ""}`;
      const existing = cart.find(c => `${c.item_id}|${c.ice}|${c.sugar}|${(c.addons || []).join(",")}|${c.note || ""}` === sig);
      if (existing) {
        existing.qty += newItem.qty;
      } else {
        cart.push(newItem);
      }
    }

    function removeCartItem(cid) {
      const u = getUser();
      const idx = u.cart.findIndex(c => c.cart_item_id === cid);
      if (idx !== -1) {
        u.cart.splice(idx, 1);
        if (isLoggedIn()) savePersistedState();
        renderHeader();
        renderCart();
      }
    }

    function clearCart() {
      const u = getUser();
      if (!u.cart.length) return;
      u.cart.length = 0;
      promoCode = "";
      if (isLoggedIn()) savePersistedState();
      renderHeader();
      renderCart();
      showToast("購物車已清空");
    }

    // ==========================================
    // 10. 付款方式、電子發票、結帳兩步驟（地址標記 → 二次確認）
    // ==========================================
    function renderPaymentUI() {
      document.getElementById("cash-payment-label").textContent =
        deliveryMode === "pickup" ? "現場現金付款" : "貨到付款（現金）";

      document.querySelectorAll('input[name="payment-method"]').forEach(r => {
        r.checked = r.value === selectedPaymentMethod;
      });
      document.getElementById("card-options-panel").classList.toggle("hidden", selectedPaymentMethod !== "card");

      // 合併系統預設卡與使用者註冊時綁定的卡片
      const u = getUser();
      const allCards = u.custom_card
        ? [{ id: "card_user", brand: u.custom_card.brand, last4: u.custom_card.last4, label: `${u.custom_card.brand} •••• ${u.custom_card.last4}（已綁定）` }, ...SAVED_CARDS]
        : SAVED_CARDS;

      if (selectedPaymentMethod === "card" && !showNewCardForm && !allCards.some(c => c.id === selectedSavedCardId)) {
        selectedSavedCardId = allCards[0].id;
      }

      document.getElementById("saved-cards-list").innerHTML = allCards.map(c => `
        <label class="flex items-center gap-2 p-2 rounded-lg bg-white border ${!showNewCardForm && selectedSavedCardId === c.id ? 'border-neutral-900' : 'border-neutral-200'} cursor-pointer">
          <input type="radio" name="saved-card" value="${c.id}" ${!showNewCardForm && selectedSavedCardId === c.id ? "checked" : ""} onchange="selectSavedCard('${c.id}')" class="accent-neutral-950" />
          <span class="font-semibold text-neutral-800">${escapeHtml(c.label)}</span>
        </label>
      `).join("");

      document.getElementById("new-card-form").classList.toggle("hidden", !showNewCardForm);
      document.getElementById("selected-payment-badge").textContent = getPaymentSummaryLabel();
    }

    function selectPaymentMethod(method) {
      selectedPaymentMethod = method;
      if (method !== "card") showNewCardForm = false;
      renderPaymentUI();
    }

    function selectSavedCard(cardId) {
      selectedSavedCardId = cardId;
      showNewCardForm = false;
      renderPaymentUI();
    }

    function toggleNewCardForm() {
      showNewCardForm = !showNewCardForm;
      renderPaymentUI();
    }

    function detectCardBrand(digits) {
      if (/^4/.test(digits)) return "VISA";
      if (/^(5[1-5]|2[2-7])/.test(digits)) return "Mastercard";
      if (/^35/.test(digits)) return "JCB";
      return digits.length ? "CARD" : "";
    }

    function formatNewCardNumber(input) {
      const digits = input.value.replace(/\D/g, "").slice(0, 16);
      input.value = digits.replace(/(.{4})/g, "$1 ").trim();
      document.getElementById("new-card-brand-tag").textContent = detectCardBrand(digits);
    }

    function formatRegCardNumber(input) {
      const digits = input.value.replace(/\D/g, "").slice(0, 16);
      input.value = digits.replace(/(.{4})/g, "$1 ").trim();
      document.getElementById("reg-card-brand").textContent = detectCardBrand(digits);
    }

    function formatCardExpiry(input) {
      const digits = input.value.replace(/\D/g, "").slice(0, 4);
      input.value = digits.length > 2 ? `${digits.slice(0, 2)}/${digits.slice(2)}` : digits;
    }

    function validatePaymentSelection() {
      if (selectedPaymentMethod === "card" && showNewCardForm) {
        const digits = document.getElementById("new-card-number").value.replace(/\D/g, "");
        const expiry = document.getElementById("new-card-expiry").value.trim();
        const cvv = document.getElementById("new-card-cvv").value.trim();
        if (digits.length < 15) {
          showToast("請輸入正確的 15~16 碼信用卡卡號");
          return false;
        }
        if (!/^(0[1-9]|1[0-2])\/\d{2}$/.test(expiry)) {
          showToast("請輸入正確的有效期限（MM/YY）");
          return false;
        }
        if (!/^\d{3,4}$/.test(cvv)) {
          showToast("請輸入 3~4 碼安全碼 CVV");
          return false;
        }
      }
      return true;
    }

    function getPaymentSummaryLabel() {
      if (selectedPaymentMethod === "cash") return deliveryMode === "pickup" ? "現場現金付款" : "貨到付款（現金）";
      if (selectedPaymentMethod === "linepay") return "LINE Pay";
      if (selectedPaymentMethod === "applepay") return "Apple Pay";
      if (selectedPaymentMethod === "jkopay") return "街口支付 JKOPay";
      if (selectedPaymentMethod === "card") {
        if (showNewCardForm) {
          const digits = document.getElementById("new-card-number").value.replace(/\D/g, "");
          const brand = detectCardBrand(digits) || "信用卡";
          return `${brand} •••• ${digits.slice(-4) || "NEW"}`;
        }
        const u = getUser();
        if (selectedSavedCardId === "card_user" && u.custom_card) {
          return `${u.custom_card.brand} •••• ${u.custom_card.last4}`;
        }
        const found = SAVED_CARDS.find(c => c.id === selectedSavedCardId) || SAVED_CARDS[0];
        return `${found.brand} •••• ${found.last4}`;
      }
      return "貨到付款";
    }

    // 電子發票與載具邏輯
    function normalizeCarrier(val) {
      let clean = (val || "").trim().toUpperCase();
      if (clean && !clean.startsWith("/")) clean = "/" + clean;
      return clean.slice(0, 8);
    }

    function isValidCarrier(val) {
      return /^\/[0-9A-Z.+\-]{7}$/.test(val);
    }

    function formatCarrierInput(input) {
      input.value = normalizeCarrier(input.value);
    }

    function handleCheckoutCarrierInput(input) {
      input.value = normalizeCarrier(input.value);
      invoiceCarrierDraft = input.value;
    }

    function selectInvoiceType(type) {
      selectedInvoiceType = type;
      renderInvoiceUI();
    }

    function setDonatePreset(code) {
      invoiceDonateCode = code;
      document.getElementById("checkout-donate-input").value = code;
    }

    function renderInvoiceUI() {
      const u = getUser();
      const boundCarrier = isLoggedIn() && u.invoice_carrier ? u.invoice_carrier : "";
      document.getElementById("invoice-bound-hint").textContent = boundCarrier ? `已綁定 ${boundCarrier}` : "";

      if (boundCarrier && !invoiceCarrierDraft) {
        invoiceCarrierDraft = boundCarrier;
      }

      ["carrier", "member", "donate", "company"].forEach(t => {
        const btn = document.getElementById(`inv-btn-${t}`);
        if (t === selectedInvoiceType) {
          btn.className = "py-2 px-2.5 rounded-lg border border-neutral-950 bg-neutral-950 text-white font-bold transition cursor-pointer";
        } else {
          btn.className = "py-2 px-2.5 rounded-lg border border-neutral-300 bg-white text-neutral-700 hover:border-neutral-500 font-semibold transition cursor-pointer";
        }
      });

      document.getElementById("inv-panel-carrier").classList.toggle("hidden", selectedInvoiceType !== "carrier");
      document.getElementById("inv-panel-donate").classList.toggle("hidden", selectedInvoiceType !== "donate");
      document.getElementById("inv-panel-company").classList.toggle("hidden", selectedInvoiceType !== "company");

      document.getElementById("checkout-carrier-input").value = invoiceCarrierDraft;
      document.getElementById("checkout-donate-input").value = invoiceDonateCode;
      document.getElementById("checkout-taxid-input").value = invoiceTaxId;
    }

    function quickBindCarrierFromCheckout() {
      if (!isLoggedIn()) {
        showToast("請先登入帳號後再綁定手機條碼載具");
        openLoginModal();
        return;
      }
      const val = normalizeCarrier(document.getElementById("checkout-carrier-input").value);
      if (!isValidCarrier(val)) {
        showToast("手機條碼格式不正確，須為 / 開頭共 8 碼（例如 /AB12345）");
        return;
      }
      getUser().invoice_carrier = val;
      invoiceCarrierDraft = val;
      savePersistedState();
      renderInvoiceUI();
      showToast(`已成功綁定手機條碼載具：${val}`);
    }

    function validateInvoiceSelection() {
      if (selectedInvoiceType === "carrier") {
        const val = normalizeCarrier(document.getElementById("checkout-carrier-input").value);
        if (!isValidCarrier(val)) {
          showToast("請輸入正確的手機條碼載具（/ 開頭共 8 碼）");
          return false;
        }
        invoiceCarrierDraft = val;
      } else if (selectedInvoiceType === "donate") {
        if (!/^\d{3,7}$/.test(invoiceDonateCode)) {
          showToast("請輸入 3~7 碼數字愛心捐贈碼");
          return false;
        }
      } else if (selectedInvoiceType === "company") {
        if (!/^\d{8}$/.test(invoiceTaxId)) {
          showToast("請輸入 8 碼公司統一編號");
          return false;
        }
      }
      return true;
    }

    function getInvoiceSummaryLabel() {
      if (selectedInvoiceType === "carrier") return `手機條碼載具（${invoiceCarrierDraft}）`;
      if (selectedInvoiceType === "donate") return `愛心捐贈碼（${invoiceDonateCode}）`;
      if (selectedInvoiceType === "company") return `公司統編（${invoiceTaxId}）`;
      return "會員雲端發票";
    }

    function handlePromoInput(val) {
      promoCode = val.trim().toUpperCase();
      renderCart();
    }

    function applyPromo() {
      const val = document.getElementById("promo-input").value.trim().toUpperCase();
      if (!val) {
        promoCode = "";
        renderCart();
        showToast("請輸入優惠碼（如 PRO85 或 VIP50）");
        return;
      }
      promoCode = val;
      renderCart();
    }

    // 啟動結帳流程 → 先開「步驟 1/2：確認地址」
    function initiateCheckout() {
      if (!isLoggedIn()) {
        showToast("請先登入帳號後再進行結帳");
        openLoginModal();
        return;
      }
      const u = getUser();
      if (!u.cart.length) {
        showToast("購物車是空的，請先加入餐點");
        return;
      }
      const summary = calculateCartSummary(u, deliveryMode, promoCode);
      if (promoCode && !summary.promo_valid) {
        showToast(summary.promo_msg || "優惠碼無效，請先清除或升級付費會員");
        return;
      }
      if (!validatePaymentSelection()) return;
      if (!validateInvoiceSelection()) return;

      pendingCheckoutData = {
        summary,
        paymentLabel: getPaymentSummaryLabel(),
        invoiceLabel: getInvoiceSummaryLabel()
      };
      openAddressModal("checkout");
    }

    // ==========================================
    // 11. 步驟 1/2：地址確認與 Google Maps 標記 Modal
    // ==========================================
    function getPrimaryCartRestaurant() {
      const u = getUser();
      if (!u.cart.length) return null;
      return RESTAURANTS.find(r => r.id === u.cart[0].restaurant_id) || null;
    }

    function updateAddressMapPreview(query) {
      const cleanQuery = (query || "").trim() || "台中市霧峰區中正路800號";
      document.getElementById("address-map-iframe").src = buildGoogleMapsEmbedUrl(cleanQuery);
      document.getElementById("address-external-map-link").href = buildGoogleMapsExternalUrl(cleanQuery);
      document.getElementById("address-pinned-label").textContent = `目前地圖標記：${cleanQuery}`;
    }

    function openAddressModal(mode = "checkout") {
      addressModalMode = mode;
      lastFocusedBeforeModal = document.activeElement;
      const u = getUser();
      const currentAddr = (isLoggedIn() && u.delivery_address)
        ? u.delivery_address
        : (isLoggedIn() && u.location_enabled && u.location_label)
          ? u.location_label
          : deliveryAddress;
      deliveryAddress = currentAddr;

      const isPickupCheckout = mode === "checkout" && deliveryMode === "pickup";
      const badgeEl = document.getElementById("address-step-badge");
      const titleEl = document.getElementById("address-modal-title");
      const subEl = document.getElementById("address-modal-subtitle");
      const deliveryControls = document.getElementById("address-delivery-controls");
      const pickupInfo = document.getElementById("address-pickup-info");
      const confirmBtn = document.getElementById("address-confirm-btn");

      if (isPickupCheckout) {
        const store = getPrimaryCartRestaurant();
        const storeName = store ? store.name : "合作門市";
        const storeAddr = store ? store.address : "台中市霧峰區中正路839號";
        badgeEl.textContent = "步驟 1/2 • 確認自取門市";
        titleEl.textContent = "確認來店自取門市地址";
        subEl.textContent = "請確認取餐門市位置，地圖已為您標記餐廳所在地址";
        deliveryControls.classList.add("hidden");
        pickupInfo.classList.remove("hidden");
        document.getElementById("pickup-store-name").textContent = storeName;
        document.getElementById("pickup-store-address").textContent = `門市地址：${storeAddr}`;
        confirmBtn.textContent = "確認門市，前往最後確認";
        updateAddressMapPreview(storeAddr);
      } else {
        badgeEl.textContent = mode === "checkout" ? "步驟 1/2 • 確認外送地址" : "設定外送地址";
        titleEl.textContent = mode === "checkout" ? "確認外送地址並於地圖標記" : "設定您的外送地址";
        subEl.textContent = "輸入或選擇送達地址，Google 地圖將即時標出配送位置";
        deliveryControls.classList.remove("hidden");
        pickupInfo.classList.add("hidden");
        document.getElementById("address-input").value = deliveryAddress;
        document.getElementById("address-note-input").value = deliveryAddressNote;
        confirmBtn.textContent = mode === "checkout" ? "確認地址，前往最後確認" : "儲存外送地址";
        updateAddressMapPreview(deliveryAddress);
      }

      document.getElementById("address-modal").classList.remove("hidden");
      updateBodyScrollLock();
      focusModal("address-modal");
    }

    function closeAddressModal() {
      document.getElementById("address-modal").classList.add("hidden");
      updateBodyScrollLock();
      restoreFocusIfAllClosed();
    }

    function pinAddressOnMap() {
      const val = document.getElementById("address-input").value.trim();
      if (!val) {
        showToast("請輸入要標記的外送地址");
        document.getElementById("address-input").focus();
        return;
      }
      updateAddressMapPreview(val);
      showToast("已在 Google 地圖標記最新地址");
    }

    function applyPresetAddress(addr) {
      document.getElementById("address-input").value = addr;
      updateAddressMapPreview(addr);
    }

    function useGpsForAddress() {
      const applyFallback = () => {
        const fallbackAddr = "台中市霧峰區中正路800號";
        document.getElementById("address-input").value = fallbackAddr;
        updateAddressMapPreview(fallbackAddr);
        showToast("已定位至目前位置（台中市霧峰區中正路800號）");
      };

      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(
          (pos) => {
            const coordQuery = `${pos.coords.latitude.toFixed(5)},${pos.coords.longitude.toFixed(5)}`;
            document.getElementById("address-input").value = coordQuery;
            updateAddressMapPreview(coordQuery);
            showToast("已透過 GPS 標記您的目前位置");
          },
          () => applyFallback(),
          { timeout: 3000 }
        );
      } else {
        applyFallback();
      }
    }

    function confirmAddressStep() {
      const isPickupCheckout = addressModalMode === "checkout" && deliveryMode === "pickup";

      if (!isPickupCheckout) {
        const inputAddr = document.getElementById("address-input").value.trim();
        if (inputAddr.length < 4) {
          showToast("請輸入完整的送達地址（至少 4 個字元）");
          document.getElementById("address-input").focus();
          return;
        }
        deliveryAddress = inputAddr;
        deliveryAddressNote = document.getElementById("address-note-input").value.trim();
        if (isLoggedIn()) {
          const u = getUser();
          u.delivery_address = deliveryAddress;
          u.delivery_address_note = deliveryAddressNote;
          savePersistedState();
        }
        renderHeader();
      }

      const prevMode = addressModalMode;
      closeAddressModal();

      if (prevMode === "checkout") {
        openCheckoutConfirmModal();
      } else if (prevMode === "profile") {
        showToast("已從地圖更新預設外送地址");
        openLoginModal();
      } else {
        showToast("外送地址已更新");
      }
    }

    // ==========================================
    // 12. 步驟 2/2：結帳最後二次確認與正式送出
    // ==========================================
    function openCheckoutConfirmModal() {
      if (!pendingCheckoutData) return;
      const u = getUser();
      const { summary, paymentLabel, invoiceLabel } = pendingCheckoutData;
      const store = getPrimaryCartRestaurant();
      const finalAddr = deliveryMode === "pickup"
        ? (store ? `${store.name}（${store.address}）` : "合作門市")
        : `${deliveryAddress}${deliveryAddressNote ? `（${deliveryAddressNote}）` : ""}`;

      document.getElementById("confirm-delivery-mode").textContent = deliveryMode === "pickup" ? "來店自取" : "外送服務";
      document.getElementById("confirm-address-title").textContent = deliveryMode === "pickup" ? "自取門市" : "外送地址";
      document.getElementById("confirm-address-text").textContent = finalAddr;
      document.getElementById("confirm-payment-label").textContent = paymentLabel;
      document.getElementById("confirm-invoice-label").textContent = invoiceLabel;

      const promoRow = document.getElementById("confirm-promo-row");
      if (summary.promo_valid && summary.discount > 0) {
        promoRow.classList.remove("hidden");
        promoRow.classList.add("flex");
        document.getElementById("confirm-promo-label").textContent = `${(promoCode || "").toUpperCase()}（折抵 $${summary.discount}）`;
      } else {
        promoRow.classList.add("hidden");
        promoRow.classList.remove("flex");
      }

      document.getElementById("confirm-items-preview").innerHTML = u.cart.map(i => `
        <div class="flex justify-between gap-2 text-neutral-700">
          <span class="truncate">[${escapeHtml(i.restaurant_name)}] ${escapeHtml(i.name)} × ${i.qty}</span>
          <span class="font-bold text-neutral-900 shrink-0">$${i.unit_price * i.qty}</span>
        </div>
      `).join("");

      document.getElementById("confirm-total-amount").textContent = `$${summary.total}`;
      document.getElementById("checkout-confirm-modal").classList.remove("hidden");
      updateBodyScrollLock();
      focusModal("checkout-confirm-modal");
    }

    function closeCheckoutConfirmModal() {
      document.getElementById("checkout-confirm-modal").classList.add("hidden");
      updateBodyScrollLock();
      restoreFocusIfAllClosed();
    }

    function reopenAddressFromConfirm() {
      closeCheckoutConfirmModal();
      openAddressModal("checkout");
    }

    function confirmAndSubmitOrder() {
      if (!isLoggedIn() || !pendingCheckoutData) return;
      const u = getUser();
      if (!u.cart.length) {
        closeCheckoutConfirmModal();
        return;
      }

      const { summary, paymentLabel, invoiceLabel } = pendingCheckoutData;
      const now = new Date();
      const store = getPrimaryCartRestaurant();
      const orderId = `ORD-${now.getFullYear()}${String(now.getMonth() + 1).padStart(2, "0")}${String(now.getDate()).padStart(2, "0")}-${String(now.getHours()).padStart(2, "0")}${String(now.getMinutes()).padStart(2, "0")}${String(now.getSeconds()).padStart(2, "0")}`;

      const newOrder = {
        order_id: orderId,
        created_at: formatDateTime(now),
        delivery_mode: deliveryMode,
        delivery_address: deliveryMode === "pickup" ? (store ? store.address : "合作門市") : deliveryAddress,
        delivery_address_note: deliveryMode === "pickup" ? "" : deliveryAddressNote,
        payment_label: paymentLabel,
        invoice_label: invoiceLabel,
        status_index: 0,
        status: getStatusSteps(deliveryMode)[0],
        items: u.cart.map(item => ({ ...item, addons: [...(item.addons || [])] })),
        subtotal: summary.subtotal,
        delivery_fee: summary.delivery_fee,
        service_fee: summary.service_fee,
        discount: summary.discount,
        total: summary.total,
        promo_code: summary.promo_valid ? (promoCode || "").toUpperCase() : ""
      };

      u.orders.unshift(newOrder);
      u.cart = [];
      promoCode = "";
      pendingCheckoutData = null;
      highlightedOrderId = orderId;
      savePersistedState();

      closeCheckoutConfirmModal();
      switchTab("orders");
      showToast("訂單已送出！餐廳已開始為您備餐");

      setTimeout(() => {
        if (highlightedOrderId === orderId) {
          highlightedOrderId = null;
          if (currentTab === "orders") renderOrders();
        }
      }, 5000);
    }

    // ==========================================
    // 13. 訂單互動（再次點購、推進狀態、自動模擬）與收藏／取餐切換
    // ==========================================
    function reorder(orderId) {
      if (!isLoggedIn()) return;
      const u = getUser();
      const target = u.orders.find(o => o.order_id === orderId);
      if (!target) return;

      target.items.forEach(item => {
        mergeItemIntoCart(u.cart, {
          ...item,
          cart_item_id: "ci_" + Date.now() + "_" + Math.random().toString(36).slice(2, 6),
          addons: [...(item.addons || [])]
        });
      });

      deliveryMode = target.delivery_mode || "delivery";
      savePersistedState();
      switchTab("cart");
      showToast("已將歷史訂單餐點加入購物車（相同規格已自動合併數量）");
    }

    function advanceOrder(orderId) {
      if (!isLoggedIn()) return;
      const u = getUser();
      const target = u.orders.find(o => o.order_id === orderId);
      if (!target || target.status_index >= 3) return;
      target.status_index += 1;
      target.status = getStatusSteps(target.delivery_mode)[target.status_index];
      savePersistedState();
      renderOrders();
      showToast(`訂單 ${orderId} 狀態更新：${target.status}`);
    }

    function toggleAutoAdvance(enabled) {
      if (autoAdvanceTimer) {
        clearInterval(autoAdvanceTimer);
        autoAdvanceTimer = null;
      }
      if (!enabled) return;
      autoAdvanceTimer = setInterval(() => {
        if (!isLoggedIn()) return;
        const u = getUser();
        const active = u.orders.find(o => o.status_index < 3);
        if (!active) return;
        active.status_index += 1;
        active.status = getStatusSteps(active.delivery_mode)[active.status_index];
        savePersistedState();
        if (currentTab === "orders") renderOrders();
      }, 8000);
    }

    function setDeliveryMode(mode) {
      deliveryMode = mode;
      renderCurrentView();
      if (activeRestaurant) renderMenuModal(false);
    }

    function toggleFavorite(rid) {
      if (!isLoggedIn()) {
        showToast("請先登入帳號即可收藏愛店至口袋名單");
        openLoginModal();
        return;
      }
      const u = getUser();
      const idx = u.favorites.indexOf(rid);
      const rest = RESTAURANTS.find(r => r.id === rid);
      const restName = rest ? rest.name : "此餐廳";

      if (idx === -1) {
        u.favorites.push(rid);
        savePersistedState();
        updateFavButtonsInDom(rid, true);
        if (currentTab === "favorites") renderFavorites();
        showToast(`已收藏「${restName}」至口袋名單`);
      } else {
        u.favorites.splice(idx, 1);
        savePersistedState();
        updateFavButtonsInDom(rid, false);
        if (currentTab === "favorites") renderFavorites();
        showToast(`已從口袋名單移除「${restName}」`, "復原", () => {
          if (!u.favorites.includes(rid)) {
            u.favorites.push(rid);
            savePersistedState();
            updateFavButtonsInDom(rid, true);
            if (currentTab === "favorites") renderFavorites();
          }
        });
      }
    }

    function updateFavButtonsInDom(rid, isFav) {
      document.querySelectorAll(`[data-fav-btn="${rid}"]`).forEach(btn => {
        btn.innerHTML = heartSvg(isFav);
        btn.setAttribute("aria-label", isFav ? "取消收藏" : "加入收藏");
      });
    }

    // ==========================================
    // 14. FoodOrder One 會員管理 Modal
    // ==========================================
    function openVipModal() {
      if (!isLoggedIn()) {
        showToast("請先登入帳號後再管理 FoodOrder One 會員");
        openLoginModal();
        return;
      }
      lastFocusedBeforeModal = document.activeElement;
      const u = getUser();
      const actions = document.getElementById("vip-modal-actions");

      if (u.is_vip) {
        actions.innerHTML = `
          <div class="p-3 rounded-xl bg-emerald-50 border border-emerald-200 text-xs text-emerald-900 font-semibold">
            您目前已是 FoodOrder One 尊榮會員，所有優惠皆已自動套用。
          </div>
          <button type="button" onclick="confirmCancelVipPrompt()" class="w-full py-2.5 bg-neutral-100 hover:bg-red-50 hover:text-red-600 text-neutral-700 rounded-xl text-xs font-bold transition cursor-pointer">
            取消訂閱（降級為一般會員）
          </button>
        `;
      } else {
        actions.innerHTML = `
          <button type="button" onclick="subscribeVip()" class="w-full py-3 bg-[#06C167] hover:bg-[#05a858] text-neutral-950 rounded-xl text-sm font-extrabold transition cursor-pointer">
            立即升級為 FoodOrder One（模擬開通）
          </button>
          <button type="button" onclick="closeVipModal()" class="w-full py-2 text-neutral-500 hover:text-neutral-800 text-xs font-semibold cursor-pointer">
            稍後再說
          </button>
        `;
      }

      document.getElementById("vip-modal").classList.remove("hidden");
      updateBodyScrollLock();
      focusModal("vip-modal");
    }

    function closeVipModal() {
      document.getElementById("vip-modal").classList.add("hidden");
      updateBodyScrollLock();
      restoreFocusIfAllClosed();
    }

    function subscribeVip() {
      if (!isLoggedIn()) return;
      getUser().is_vip = true;
      savePersistedState();
      closeVipModal();
      renderCurrentView();
      showToast("歡迎加入 FoodOrder One！已自動享免運與專屬折扣碼");
    }

    function confirmCancelVipPrompt() {
      document.getElementById("vip-modal-actions").innerHTML = `
        <div class="p-3 rounded-xl bg-red-50 border border-red-200 text-xs text-red-800">
          確定要取消訂閱嗎？降級為一般會員後將恢復 $39 外送費與 $15 平台服務費。
        </div>
        <div class="flex gap-2">
          <button type="button" onclick="openVipModal()" class="flex-1 py-2.5 bg-neutral-100 rounded-xl text-xs font-bold cursor-pointer">保留會員</button>
          <button type="button" onclick="cancelVip()" class="flex-1 py-2.5 bg-red-600 hover:bg-red-700 text-white rounded-xl text-xs font-bold cursor-pointer">確定取消訂閱</button>
        </div>
      `;
    }

    function cancelVip() {
      if (!isLoggedIn()) return;
      getUser().is_vip = false;
      savePersistedState();
      closeVipModal();
      renderCurrentView();
      showToast("已取消 FoodOrder One 訂閱，切換為一般會員");
    }

    // ==========================================
    // 15. 登入、個人資料修改、載具綁定與登出
    // ==========================================
    let currentAccountTab = "profile";

    function openLoginModal() {
      lastFocusedBeforeModal = document.activeElement;
      currentAccountTab = "profile";
      renderLoginModalContent();
      document.getElementById("login-modal").classList.remove("hidden");
      updateBodyScrollLock();
      focusModal("login-modal");
    }

    function closeLoginModal() {
      document.getElementById("login-modal").classList.add("hidden");
      updateBodyScrollLock();
      restoreFocusIfAllClosed();
    }

    function switchAccountTab(tab) {
      currentAccountTab = tab;
      const isProfile = tab === "profile";
      document.getElementById("acct-panel-profile").classList.toggle("hidden", !isProfile);
      document.getElementById("acct-panel-bindings").classList.toggle("hidden", isProfile);

      document.getElementById("acct-tab-profile").className = isProfile
        ? "py-2 rounded-lg bg-white text-neutral-950 shadow-sm transition cursor-pointer"
        : "py-2 rounded-lg text-neutral-500 hover:text-neutral-800 transition cursor-pointer";
      document.getElementById("acct-tab-bindings").className = !isProfile
        ? "py-2 rounded-lg bg-white text-neutral-950 shadow-sm transition cursor-pointer"
        : "py-2 rounded-lg text-neutral-500 hover:text-neutral-800 transition cursor-pointer";
    }

    function renderLoginModalContent() {
      const loggedIn = isLoggedIn();
      document.getElementById("login-modal-title").textContent = loggedIn ? "我的帳號與個人設定" : "會員登入";
      document.getElementById("login-guest-view").classList.toggle("hidden", loggedIn);
      document.getElementById("login-authed-view").classList.toggle("hidden", !loggedIn);

      if (loggedIn) {
        const u = getUser();
        const avatarCircle = document.getElementById("acct-avatar-circle");
        avatarCircle.textContent = (u.display_name || "U").charAt(0).toUpperCase();
        avatarCircle.className = u.google_email
          ? "w-12 h-12 rounded-full bg-blue-600 text-white font-extrabold text-lg flex items-center justify-center shrink-0"
          : "w-12 h-12 rounded-full bg-neutral-900 text-white font-extrabold text-lg flex items-center justify-center shrink-0";

        document.getElementById("acct-display-name").textContent = u.display_name;
        document.getElementById("acct-username").textContent = `帳號：@${u.username}`;

        const vipTag = document.getElementById("acct-vip-tag");
        if (u.is_vip) {
          vipTag.textContent = "One 付費會員";
          vipTag.className = "text-[11px] font-bold px-2.5 py-0.5 rounded-full bg-[#06C167] text-neutral-950 shrink-0";
        } else {
          vipTag.textContent = "一般會員";
          vipTag.className = "text-[11px] font-bold px-2.5 py-0.5 rounded-full bg-neutral-200 text-neutral-700 shrink-0";
        }

        // 填入個人資料修改表單（點頭像進來就能直接修改）
        const userAddr = u.delivery_address || deliveryAddress;
        document.getElementById("acct-edit-name").value = u.display_name || "";
        document.getElementById("acct-edit-phone").value = u.phone || "";
        document.getElementById("acct-edit-birthday").value = u.birthday || "";
        document.getElementById("acct-edit-address").value = userAddr || "";
        document.getElementById("acct-edit-address-note").value = u.delivery_address_note || "";

        // Google 帳號繫結狀態
        const gStatus = document.getElementById("acct-google-status");
        const gEmail = document.getElementById("acct-google-email");
        const gActions = document.getElementById("acct-google-actions");
        if (u.google_email) {
          gStatus.textContent = "已繫結";
          gStatus.className = "text-[11px] font-bold text-[#059652]";
          gEmail.textContent = `已連結 Google 帳戶：${u.google_email}`;
          gActions.innerHTML = `<button type="button" onclick="unbindGoogleAccount()" class="text-[11px] font-semibold text-red-600 hover:underline cursor-pointer">解除 Google 繫結</button>`;
        } else {
          gStatus.textContent = "未繫結";
          gStatus.className = "text-[11px] font-semibold text-neutral-400";
          gEmail.textContent = "繫結後可使用 Google 帳戶一鍵快速登入。";
          gActions.innerHTML = `<button type="button" onclick="openGoogleOAuthModal('bind')" class="mt-1 px-3 py-1.5 bg-neutral-900 hover:bg-neutral-800 text-white rounded-lg text-xs font-semibold cursor-pointer">立即繫結 Google 帳號</button>`;
        }

        // 載具狀態
        const cStatus = document.getElementById("acct-carrier-status");
        const cInput = document.getElementById("acct-carrier-input");
        const cUnbind = document.getElementById("acct-carrier-unbind-btn");
        if (u.invoice_carrier) {
          cStatus.textContent = "已綁定";
          cStatus.className = "text-[11px] font-bold text-[#059652]";
          cInput.value = u.invoice_carrier;
          cUnbind.classList.remove("hidden");
        } else {
          cStatus.textContent = "未綁定";
          cStatus.className = "text-[11px] font-semibold text-neutral-400";
          cInput.value = "";
          cUnbind.classList.add("hidden");
        }

        switchAccountTab(currentAccountTab);
      }
    }

    function saveAccountProfile() {
      if (!isLoggedIn()) return;
      const name = document.getElementById("acct-edit-name").value.trim();
      const phone = document.getElementById("acct-edit-phone").value.trim();
      const birthday = document.getElementById("acct-edit-birthday").value;
      const address = document.getElementById("acct-edit-address").value.trim();
      const addressNote = document.getElementById("acct-edit-address-note").value.trim();

      if (!name) {
        showToast("姓名不可為空");
        document.getElementById("acct-edit-name").focus();
        return;
      }
      if (phone && !/^09\d{8}$/.test(phone)) {
        showToast("手機號碼格式不正確（請輸入 09 開頭共 10 碼，或留空）");
        document.getElementById("acct-edit-phone").focus();
        return;
      }
      if (address.length < 4) {
        showToast("請輸入完整的預設外送地址（至少 4 個字元）");
        document.getElementById("acct-edit-address").focus();
        return;
      }

      const u = getUser();
      u.display_name = name;
      u.phone = phone;
      u.birthday = birthday;
      u.delivery_address = address;
      u.delivery_address_note = addressNote;

      deliveryAddress = address;
      deliveryAddressNote = addressNote;

      savePersistedState();
      renderLoginModalContent();
      renderHeader();
      showToast("個人資料已更新並儲存");
    }

    function openMapFromProfileEdit() {
      closeLoginModal();
      openAddressModal("profile");
    }

    function saveAccountCarrier() {
      if (!isLoggedIn()) return;
      const val = normalizeCarrier(document.getElementById("acct-carrier-input").value);
      if (!isValidCarrier(val)) {
        showToast("手機條碼格式不正確，須為 / 開頭共 8 碼（例如 /AB12345）");
        return;
      }
      getUser().invoice_carrier = val;
      invoiceCarrierDraft = val;
      savePersistedState();
      renderLoginModalContent();
      if (currentTab === "cart") renderCart();
      showToast(`已成功綁定手機條碼載具：${val}`);
    }

    function unbindAccountCarrier() {
      if (!isLoggedIn()) return;
      getUser().invoice_carrier = "";
      invoiceCarrierDraft = "";
      savePersistedState();
      renderLoginModalContent();
      if (currentTab === "cart") renderCart();
      showToast("已解除手機條碼載具綁定");
    }

    function mergeGuestCartToUser(user) {
      if (!GUEST_CART.length) return;
      GUEST_CART.forEach(item => mergeItemIntoCart(user.cart, item));
      GUEST_CART = [];
    }

    function completeUserLogin(userKey) {
      CURRENT_USER_KEY = userKey;
      const u = USERS[userKey];
      mergeGuestCartToUser(u);
      if (u.delivery_address) {
        deliveryAddress = u.delivery_address;
        deliveryAddressNote = u.delivery_address_note || "";
      }
      if (u.invoice_carrier) {
        invoiceCarrierDraft = u.invoice_carrier;
        selectedInvoiceType = "carrier";
      }
      if (u.custom_card) {
        selectedPaymentMethod = "card";
        selectedSavedCardId = "card_user";
      }
      promoCode = "";
      savePersistedState();
      closeLoginModal();
      renderCurrentView();
      showToast(`歡迎回來，${u.display_name}！`);
    }

    function submitLogin() {
      const rawUser = document.getElementById("login-username").value.trim().toLowerCase();
      const display = document.getElementById("login-display").value.trim();
      if (!/^[a-z0-9_]{3,20}$/.test(rawUser)) {
        showToast("帳號須為 3~20 碼英數字或底線（例如 student01）");
        return;
      }

      if (!USERS[rawUser]) {
        USERS[rawUser] = {
          username: rawUser,
          display_name: display || rawUser,
          birthday: "",
          phone: "",
          custom_card: null,
          location_enabled: false,
          location_label: "",
          delivery_address: deliveryAddress,
          delivery_address_note: "",
          google_email: null,
          invoice_carrier: "",
          is_vip: false,
          favorites: [],
          cart: [],
          orders: []
        };
      } else if (display) {
        USERS[rawUser].display_name = display;
      }

      document.getElementById("login-username").value = "";
      document.getElementById("login-display").value = "";
      completeUserLogin(rawUser);
    }

    function quickDemoLogin() {
      if (!USERS.student01) {
        USERS.student01 = createDefaultUsers().student01;
      }
      completeUserLogin("student01");
    }

    function logoutUser() {
      CURRENT_USER_KEY = null;
      promoCode = "";
      invoiceCarrierDraft = "";
      savePersistedState();
      closeLoginModal();
      renderCurrentView();
      showToast("已成功登出帳號");
    }

    // ==========================================
    // 16. Google OAuth 登入與繫結模擬
    // ==========================================
    function openGoogleOAuthModal(mode = "login") {
      googleOAuthMode = mode;
      document.getElementById("custom-google-email").value = "";
      document.getElementById("google-oauth-modal").classList.remove("hidden");
      updateBodyScrollLock();
      focusModal("google-oauth-modal");
    }

    function closeGoogleOAuthModal() {
      document.getElementById("google-oauth-modal").classList.add("hidden");
      updateBodyScrollLock();
    }

    function selectGoogleAccount(name, email) {
      const normalizedEmail = email.trim().toLowerCase();
      if (googleOAuthMode === "bind" && isLoggedIn()) {
        getUser().google_email = normalizedEmail;
        savePersistedState();
        closeGoogleOAuthModal();
        renderLoginModalContent();
        renderHeader();
        showToast(`已成功繫結 Google 帳戶：${normalizedEmail}`);
        return;
      }

      // 登入模式：尋找是否已有綁定此 Gmail 的使用者
      let existingKey = Object.keys(USERS).find(k => (USERS[k].google_email || "").toLowerCase() === normalizedEmail);
      if (!existingKey) {
        const baseKey = normalizedEmail.split("@")[0].replace(/[^a-z0-9_]/g, "_").slice(0, 16) || "google_user";
        existingKey = USERS[baseKey] ? `${baseKey}_${Date.now().toString().slice(-3)}` : baseKey;
        USERS[existingKey] = {
          username: existingKey,
          display_name: name || baseKey,
          birthday: "",
          phone: "",
          custom_card: null,
          location_enabled: false,
          location_label: "",
          delivery_address: deliveryAddress,
          delivery_address_note: "",
          google_email: normalizedEmail,
          invoice_carrier: "",
          is_vip: false,
          favorites: [],
          cart: [],
          orders: []
        };
      }
      closeGoogleOAuthModal();
      completeUserLogin(existingKey);
    }

    function submitCustomGoogleAccount() {
      const email = document.getElementById("custom-google-email").value.trim().toLowerCase();
      if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
        showToast("請輸入有效的 Email 格式（例如 yourname@gmail.com）");
        return;
      }
      selectGoogleAccount(email.split("@")[0], email);
    }

    function unbindGoogleAccount() {
      if (!isLoggedIn()) return;
      getUser().google_email = null;
      savePersistedState();
      renderLoginModalContent();
      renderHeader();
      showToast("已解除 Google 帳號繫結");
    }

    // ==========================================
    // 17. 三步驟會員註冊系統
    // ==========================================
    function openRegisterModal() {
      closeLoginModal();
      regStep = 1;
      regDraft = { username: "", name: "", birthday: "", phone: "", custom_card: null, location_enabled: false, location_label: "" };
      ["reg-username", "reg-name", "reg-birthday", "reg-phone", "reg-card-number", "reg-card-expiry", "reg-card-cvv"].forEach(id => {
        const el = document.getElementById(id);
        if (el) el.value = "";
      });
      document.getElementById("reg-card-brand").textContent = "";
      renderRegStepUI();
      document.getElementById("register-modal").classList.remove("hidden");
      updateBodyScrollLock();
      focusModal("register-modal");
    }

    function closeRegisterModal() {
      document.getElementById("register-modal").classList.add("hidden");
      updateBodyScrollLock();
      restoreFocusIfAllClosed();
    }

    function renderRegStepUI() {
      const titles = {
        1: "建立新帳號：綁定基本資料",
        2: "新增常用信用卡（可跳過）",
        3: "開啟定位服務"
      };
      document.getElementById("reg-step-badge").textContent = `步驟 ${regStep} / 3`;
      document.getElementById("reg-modal-title").textContent = titles[regStep];

      [1, 2, 3].forEach(n => {
        document.getElementById(`reg-step-${n}`).classList.toggle("hidden", n !== regStep);
        document.getElementById(`reg-bar-${n}`).className = n <= regStep
          ? "h-1.5 rounded-full bg-[#06C167] transition"
          : "h-1.5 rounded-full bg-neutral-200 transition";
      });
    }

    function nextRegStep1() {
      const username = document.getElementById("reg-username").value.trim().toLowerCase();
      const name = document.getElementById("reg-name").value.trim();
      const birthday = document.getElementById("reg-birthday").value;
      const phone = document.getElementById("reg-phone").value.trim();

      if (!/^[a-z0-9_]{3,20}$/.test(username)) {
        showToast("登入帳號須為 3~20 碼英數字或底線");
        return;
      }
      if (USERS[username]) {
        showToast("此帳號已被註冊，請換一個帳號或直接登入");
        return;
      }
      if (!name) {
        showToast("請輸入真實姓名");
        return;
      }
      if (!birthday) {
        showToast("請選擇出生日期");
        return;
      }
      if (!/^09\d{8}$/.test(phone)) {
        showToast("請輸入正確的 10 碼台灣手機號碼（09 開頭）");
        return;
      }

      regDraft.username = username;
      regDraft.name = name;
      regDraft.birthday = birthday;
      regDraft.phone = phone;
      regStep = 2;
      renderRegStepUI();
    }

    function nextRegStep2(skip) {
      if (skip) {
        regDraft.custom_card = null;
      } else {
        const digits = document.getElementById("reg-card-number").value.replace(/\D/g, "");
        const expiry = document.getElementById("reg-card-expiry").value.trim();
        const cvv = document.getElementById("reg-card-cvv").value.trim();
        if (digits.length < 15) {
          showToast("請輸入 15~16 碼有效信用卡號，或點下方跳過此步驟");
          return;
        }
        if (!/^(0[1-9]|1[0-2])\/\d{2}$/.test(expiry)) {
          showToast("請輸入正確的有效期限（MM/YY）");
          return;
        }
        if (!/^\d{3,4}$/.test(cvv)) {
          showToast("請輸入 3~4 碼安全碼 CVV");
          return;
        }
        regDraft.custom_card = {
          brand: detectCardBrand(digits) || "VISA",
          last4: digits.slice(-4),
          expiry
        };
      }
      regStep = 3;
      renderRegStepUI();
    }

    function finishRegistration(enableLocation) {
      const finalize = (locEnabled, locAddr) => {
        const newUser = {
          username: regDraft.username,
          display_name: regDraft.name,
          birthday: regDraft.birthday,
          phone: regDraft.phone,
          custom_card: regDraft.custom_card,
          location_enabled: locEnabled,
          location_label: locEnabled ? locAddr : "",
          delivery_address: locAddr,
          delivery_address_note: "",
          google_email: null,
          invoice_carrier: "",
          is_vip: false,
          favorites: [],
          cart: [],
          orders: []
        };
        USERS[newUser.username] = newUser;
        closeRegisterModal();
        completeUserLogin(newUser.username);
        showToast(`註冊成功！歡迎加入 FoodOrder，${newUser.display_name}`);
      };

      if (!enableLocation) {
        finalize(false, "台中市霧峰區中正路800號");
        return;
      }

      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(
          () => finalize(true, "台中市霧峰區中正路800號"),
          () => finalize(true, "台中市霧峰區中正路800號"),
          { timeout: 2500 }
        );
      } else {
        finalize(true, "台中市霧峰區中正路800號");
      }
    }

    // ==========================================
    // 18. 應用程式初始化
    // ==========================================
    loadPersistedState();
    if (isLoggedIn() && getUser().delivery_address) {
      deliveryAddress = getUser().delivery_address;
      deliveryAddressNote = getUser().delivery_address_note || "";
    }
    switchTab("home", false);
  </script>
</body>
</html>