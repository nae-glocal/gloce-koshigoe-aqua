<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>鎌倉市腰越エリア：ゲストハウス事業フィージビリティ調査</title>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700;900&display=swap" rel="stylesheet">
<style>
    body { font-family: 'Noto Sans JP', sans-serif; background-color: #F8FAFC; color: #0F172A; }
    .chart-container { position: relative; width: 100%; max-width: 800px; margin-left: auto; margin-right: auto; height: 350px; max-height: 400px; }
    @media (min-width: 768px) { .chart-container { height: 400px; } }
    .swot-box { transition: transform 0.2s; }
    .swot-box:hover { transform: translateY(-5px); }
</style>
</head>
<body class="antialiased">
<!-- Palette: Energetic Coastal (Deep Blue: #1E3A8A, Vibrant Cyan: #06B6D4, Golden Yellow: #EAB308, Coral Red: #EF4444) -->
<!-- Narrative Plan: 1. Executive KPIs (Context) -> 2. Occupancy Trends (Change) -> 3. Demographics (Compare) -> 4. SWOT Feasibility (Organize) -> 5. Marketing Funnel (Process Flow) -->
<!-- CONFIRMATION: NEITHER Mermaid JS NOR SVG were used anywhere in this output. All icons use Unicode, all charts use Canvas. -->

<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
    <header class="mb-12 text-center">
        <h1 class="text-4xl md:text-5xl font-black text-[#1E3A8A] tracking-tight mb-4">鎌倉市腰越エリア<br><span class="text-[#06B6D4]">宿泊事業ポテンシャル分析</span></h1>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto font-bold">対象地：神奈川県鎌倉市腰越２丁目２番２号</p>
        <p class="mt-4 text-gray-600 max-w-3xl mx-auto">江ノ電「腰越駅」至近、湘南海岸エリアにおけるゲストハウス開業に向けた市場動向、稼働率予測、およびマーケティング戦略の視覚的レポート。</p>
    </header>

    <section class="mb-16">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
            <div class="bg-white rounded-2xl shadow-lg p-6 border-l-4 border-[#1E3A8A]">
                <div class="text-4xl mb-2">&#128205;</div>
                <h3 class="text-sm font-bold text-gray-500 uppercase tracking-wider">立地アドバンテージ</h3>
                <p class="text-3xl font-black text-[#1E3A8A] mt-2">徒歩3分圏内</p>
                <p class="text-sm text-gray-600 mt-2">腰越駅・海岸までのアクセスが極めて良好。マリンスポーツ層に最適。</p>
            </div>
            <div class="bg-white rounded-2xl shadow-lg p-6 border-l-4 border-[#06B6D4]">
                <div class="text-4xl mb-2">&#128101;</div>
                <h3 class="text-sm font-bold text-gray-500 uppercase tracking-wider">鎌倉市年間観光客数</h3>
                <p class="text-3xl font-black text-[#06B6D4] mt-2">約2,000万人</p>
                <p class="text-sm text-gray-600 mt-2">日帰り客が中心だが、江ノ島・鎌倉周遊のハブとして宿泊需要の取り込み余地あり。</p>
            </div>
            <div class="bg-white rounded-2xl shadow-lg p-6 border-l-4 border-[#EAB308]">
                <div class="text-4xl mb-2">&#128200;</div>
                <h3 class="text-sm font-bold text-gray-500 uppercase tracking-wider">推定年間平均稼働率</h3>
                <p class="text-3xl font-black text-[#EAB308] mt-2">55% - 65%</p>
                <p class="text-sm text-gray-600 mt-2">季節変動が激しいため、通年での平均化戦略が事業成功の鍵。</p>
            </div>
            <div class="bg-white rounded-2xl shadow-lg p-6 border-l-4 border-[#EF4444]">
                <div class="text-4xl mb-2">&#127960;</div>
                <h3 class="text-sm font-bold text-gray-500 uppercase tracking-wider">事業成立の可能性</h3>
                <p class="text-3xl font-black text-[#EF4444] mt-2">十分に可能</p>
                <p class="text-sm text-gray-600 mt-2">ただし、単なる「安宿」ではなく、体験型コンテンツの付帯が必須条件。</p>
            </div>
        </div>
    </section>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-16">
        <section class="bg-white p-8 rounded-2xl shadow-lg">
            <h2 class="text-2xl font-bold text-[#1E3A8A] mb-4 border-b-2 border-gray-100 pb-2">季節ごとの稼働率予測（繁忙期 vs 閑散期）</h2>
            <p class="mb-6 text-gray-600 text-sm">
                湘南エリアの特徴として、<strong>7月〜8月の夏季およびゴールデンウィークが圧倒的な繁忙期</strong>となり、稼働率は80%〜90%以上に達します。一方、1月〜2月の冬季は閑散期となり、40%台まで落ち込むリスクがあります。
            </p>
            <div class="chart-container">
                <canvas id="occupancyChart"></canvas>
            </div>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-lg">
            <h2 class="text-2xl font-bold text-[#1E3A8A] mb-4 border-b-2 border-gray-100 pb-2">ターゲット顧客層（ゲストハウス想定）</h2>
            <p class="mb-6 text-gray-600 text-sm">
                腰越という立地特性上、サーフィン等を目的とする<strong>国内若年層・アクティブ層</strong>がメインとなります。次いで、スラムダンクの聖地巡礼（鎌倉高校前駅近接）等を目的とした<strong>インバウンド旅行客</strong>が有力なターゲットです。
            </p>
            <div class="chart-container">
                <canvas id="demographicsChart"></canvas>
            </div>
        </section>
    </div>

    <section class="mb-16">
        <h2 class="text-3xl font-bold text-center text-[#1E3A8A] mb-10">腰越２丁目 ゲストハウス事業 SWOT分析</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="swot-box bg-blue-50 border-t-8 border-[#1E3A8A] p-8 rounded-xl shadow-md">
                <h3 class="text-2xl font-black text-[#1E3A8A] mb-4">S <span class="text-lg font-bold text-gray-700 ml-2">強み (Strengths)</span></h3>
                <ul class="space-y-3">
                    <li class="flex items-start"><span class="text-[#1E3A8A] font-bold mr-2">&#10003;</span> 江ノ電駅、海岸、漁港が至近の圧倒的なロケーション</li>
                    <li class="flex items-start"><span class="text-[#1E3A8A] font-bold mr-2">&#10003;</span> 湘南のローカル感（しらす漁など）を体験できる環境</li>
                    <li class="flex items-start"><span class="text-[#1E3A8A] font-bold mr-2">&#10003;</span> 土地所有による初期投資（不動産取得費）の圧縮</li>
                </ul>
            </div>
            <div class="swot-box bg-red-50 border-t-8 border-[#EF4444] p-8 rounded-xl shadow-md">
                <h3 class="text-2xl font-black text-[#EF4444] mb-4">W <span class="text-lg font-bold text-gray-700 ml-2">弱み (Weaknesses)</span></h3>
                <ul class="space-y-3">
                    <li class="flex items-start"><span class="text-[#EF4444] font-bold mr-2">&#10007;</span> 季節変動への依存度が高い（夏への偏重）</li>
                    <li class="flex items-start"><span class="text-[#EF4444] font-bold mr-2">&#10007;</span> 騒音問題など近隣住民（住宅街）とのトラブルリスク</li>
                    <li class="flex items-start"><span class="text-[#EF4444] font-bold mr-2">&#10007;</span> 鎌倉駅周辺と比較すると夜間の飲食の選択肢が限られる</li>
                </ul>
            </div>
            <div class="swot-box bg-yellow-50 border-t-8 border-[#EAB308] p-8 rounded-xl shadow-md">
                <h3 class="text-2xl font-black text-[#EAB308] mb-4">O <span class="text-lg font-bold text-gray-700 ml-2">機会 (Opportunities)</span></h3>
                <ul class="space-y-3">
                    <li class="flex items-start"><span class="text-[#EAB308] font-bold mr-2">&#10148;</span> ワーケーション需要の取り込み（長期滞在・閑散期対策）</li>
                    <li class="flex items-start"><span class="text-[#EAB308] font-bold mr-2">&#10148;</span> アニメ聖地巡礼によるアジア圏インバウンドの増加</li>
                    <li class="flex items-start"><span class="text-[#EAB308] font-bold mr-2">&#10148;</span> 地元漁港や飲食店との連携による体験パッケージ化</li>
                </ul>
            </div>
            <div class="swot-box bg-gray-50 border-t-8 border-gray-600 p-8 rounded-xl shadow-md">
                <h3 class="text-2xl font-black text-gray-600 mb-4">T <span class="text-lg font-bold text-gray-700 ml-2">脅威 (Threats)</span></h3>
                <ul class="space-y-3">
                    <li class="flex items-start"><span class="text-gray-600 font-bold mr-2">&#9888;</span> 津波・高潮などの自然災害リスク（ハザードマップ要確認）</li>
                    <li class="flex items-start"><span class="text-gray-600 font-bold mr-2">&#9888;</span> 周辺の民泊・新規ホテルの増加による価格競争</li>
                    <li class="flex items-start"><span class="text-gray-600 font-bold mr-2">&#9888;</span> 法規制（旅館業法・民泊新法）の厳格化</li>
                </ul>
            </div>
        </div>
    </section>

    <section class="bg-[#1E3A8A] rounded-3xl p-10 text-white shadow-xl mb-16">
        <h2 class="text-3xl font-bold mb-8 text-center border-b border-blue-800 pb-4">推奨マーケティング＆集客フロー</h2>
        <p class="text-center mb-10 text-blue-200">閑散期の落ち込みを防ぎ、通年で安定した稼働を維持するための戦略的ファンネル</p>
        
        <div class="flex flex-col lg:flex-row items-center justify-between space-y-6 lg:space-y-0 lg:space-x-4">
            
            <div class="bg-white text-[#1E3A8A] rounded-xl p-6 w-full lg:w-1/4 text-center relative shadow-lg">
                <div class="text-4xl mb-3">&#128248;</div>
                <h4 class="font-bold text-xl mb-2">1. 認知獲得</h4>
                <p class="text-sm font-semibold text-[#06B6D4] mb-2">Instagram / TikTok</p>
                <p class="text-xs text-gray-600">江ノ電、海、夕日などの「映え」コンテンツと、ローカルな湘南ライフスタイルの発信。</p>
            </div>

            <div class="text-3xl text-[#06B6D4] rotate-90 lg:rotate-0">&#10140;</div>

            <div class="bg-white text-[#1E3A8A] rounded-xl p-6 w-full lg:w-1/4 text-center relative shadow-lg">
                <div class="text-4xl mb-3">&#128187;</div>
                <h4 class="font-bold text-xl mb-2">2. 比較・検討</h4>
                <p class="text-sm font-semibold text-[#06B6D4] mb-2">OTA最適化</p>
                <p class="text-xs text-gray-600">Airbnb, Booking.comでの上位表示。多言語対応と、プロによる魅力的な施設写真の掲載。</p>
            </div>

            <div class="text-3xl text-[#06B6D4] rotate-90 lg:rotate-0">&#10140;</div>

            <div class="bg-white text-[#1E3A8A] rounded-xl p-6 w-full lg:w-1/4 text-center relative shadow-lg">
                <div class="text-4xl mb-3">&#127940;</div>
                <h4 class="font-bold text-xl mb-2">3. 予約・体験</h4>
                <p class="text-sm font-semibold text-[#06B6D4] mb-2">付加価値の提供</p>
                <p class="text-xs text-gray-600">単なる宿泊ではなく、SUP体験、地元しらす丼朝食、ワーケーション設備等のプラン化。</p>
            </div>

            <div class="text-3xl text-[#06B6D4] rotate-90 lg:rotate-0">&#10140;</div>

            <div class="bg-white text-[#1E3A8A] rounded-xl p-6 w-full lg:w-1/4 text-center relative shadow-lg">
                <div class="text-4xl mb-3">&#11088;</div>
                <h4 class="font-bold text-xl mb-2">4. 共有・リピート</h4>
                <p class="text-sm font-semibold text-[#06B6D4] mb-2">コミュニティ化</p>
                <p class="text-xs text-gray-600">高評価レビューの促進。リピーター向け割引や、定期的なローカルイベントの案内。</p>
            </div>

        </div>
    </section>

    <footer class="text-center text-gray-500 text-sm mt-12 pb-8 border-t border-gray-200 pt-8">
        <p>※本データは湘南・鎌倉エリアの一般的な観光統計および市場トレンドに基づく予測値であり、実際の事業収益を保証するものではありません。<br>事業化の際は、詳細な建築法規確認および精緻な収支シミュレーションを推奨します。</p>
    </footer>

</div>

<script>
    function wrapLabels(labels) {
        return labels.map(label => {
            if (label.length <= 16) return label;
            const words = label.split(' ');
            let lines = [];
            let currentLine = '';
            words.forEach(word => {
                if ((currentLine + word).length > 16) {
                    if (currentLine) lines.push(currentLine.trim());
                    currentLine = word + ' ';
                } else {
                    currentLine += word + ' ';
                }
            });
            if (currentLine) lines.push(currentLine.trim());
            return lines;
        });
    }

    const commonTooltip = {
        callbacks: {
            title: function(tooltipItems) {
                const item = tooltipItems[0];
                let label = item.chart.data.labels[item.dataIndex];
                if (Array.isArray(label)) {
                    return label.join(' ');
                } else {
                    return label;
                }
            }
        }
    };

    const occCtx = document.getElementById('occupancyChart').getContext('2d');
    const rawOccLabels = ['1月 (Jan)', '2月 (Feb)', '3月 (Mar)', '4月 (Apr)', '5月 (May/GW)', '6月 (Jun)', '7月 (Jul)', '8月 (Aug)', '9月 (Sep)', '10月 (Oct)', '11月 (Nov)', '12月 (Dec)'];
    
    new Chart(occCtx, {
        type: 'line',
        data: {
            labels: wrapLabels(rawOccLabels),
            datasets: [{
                label: '想定月間稼働率 (%)',
                data: [42, 45, 60, 65, 82, 55, 85, 92, 70, 65, 55, 50],
                borderColor: '#06B6D4',
                backgroundColor: 'rgba(6, 182, 212, 0.2)',
                borderWidth: 3,
                pointBackgroundColor: '#1E3A8A',
                pointRadius: 5,
                fill: true,
                tension: 0.4
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: { position: 'top' },
                tooltip: commonTooltip
            },
            scales: {
                y: {
                    beginAtZero: true,
                    max: 100,
                    title: { display: true, text: '稼働率 (%)' }
                }
            }
        }
    });

    const demoCtx = document.getElementById('demographicsChart').getContext('2d');
    const rawDemoLabels = ['国内マリンスポーツ層・若年層', 'インバウンド・聖地巡礼客', '国内ワーケーション・単身客', 'ファミリー・グループ層'];
    
    new Chart(demoCtx, {
        type: 'doughnut',
        data: {
            labels: wrapLabels(rawDemoLabels),
            datasets: [{
                data: [45, 30, 15, 10],
                backgroundColor: [
                    '#1E3A8A',
                    '#06B6D4',
                    '#EAB308',
                    '#EF4444'
                ],
                borderWidth: 2,
                borderColor: '#ffffff'
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            cutout: '65%',
            plugins: {
                legend: { position: 'right' },
                tooltip: commonTooltip
            }
        }
    });
</script>
</body>
</html>
