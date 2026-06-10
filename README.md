# CS351 — 課程儲存庫
**學生：** Huang Yen-Chun (Cyan) · GitHub: [Cyanlit](https://github.com/Cyanlit)
**課程：** CS351 — AI 輔助軟體開發 · 元智大學
 
---
 
## 目錄
1. [個人網站](#1-個人網站)
2. [課程成果與學習紀錄](#2-課程成果與學習紀錄)
3. [Project 0 — Two Sum](#3-project-0--two-sum)
4. [Project B — CSV 迷你資料庫與查詢引擎](#4-project-b--csv-迷你資料庫與查詢引擎)
5. [GitHub 工作流程證據](#5-github-工作流程證據)
6. [AI 輔助開發反思](#6-ai-輔助開發反思)
---
## 連結速覽
 
| 項目 | 連結 |
|------|------|
| 課程儲存庫（本 repo） | https://github.com/Cyanlit/11402_CS351 |
| 個人網站 | https://cyanlit.github.io/ |
| 個人網站原始碼 | https://github.com/Cyanlit/Cyanlit.github.io |
| Project 0（Two Sum） | https://github.com/Cyanlit/11402_CS351_Project0 |
| Project B（CSV 查詢引擎） | https://github.com/Cyanlit/11402_CS351_ProjectB |
| 課程官方參考 | https://github.com/yfhuang/YZUCSE_CS351 |

## 1. 個人網站
 
**網址：** https://cyanlit.github.io/
**Repo：** https://github.com/Cyanlit/Cyanlit.github.io
 
### 使用技術
| 層級 | 選擇 |
|-------|--------|
| 標記語言 | HTML5（單頁、語意化結構） |
| 樣式 | 內嵌／輕量 CSS — 乾淨、極簡、以文字為主的版面 |
| 託管 | GitHub Pages（透過 `Cyanlit.github.io` 提供免費靜態網站託管） |
| 素材 | 個人大頭照，加上以個人簡介形式呈現的 README 內容作為頁面主體 |
 
### 設計理念
- **極簡學術風格簡介** — 整體呈現比較像個人履歷／研究自述頁面，而非花俏的作品集，呼應重視 CS 基礎勝過視覺效果的取向
- **以內容為主的版面配置** — 各區塊依序為：自我介紹 → 興趣領域 → 技術背景 → 個人理念，類似教師或研究生個人首頁的結構
- **單一大頭照搭配文字區塊** — 不依賴大量圖形或動畫，讓頁面在任何裝置上都輕量且易讀
- **回連 GitHub 個人頁面** — 將靜態網站與實際的 GitHub 帳號串連起來
### 內容重點
- **About Me** — 介紹作者為大四資工學生，專注於資料結構、演算法、作業系統、計算機組織與軟體開發，同時對底層實作細節與整體系統架構都有興趣
- **Areas of Interest** — 資料結構與演算法、系統程式設計、後端開發
- **Technical Background** — 程式語言：C++、Python、TypeScript；系統相關：Git／版本控制、基礎網路概念
- **Philosophy** — 強調紮實的基礎是長期成長的根本，而這需要透過有紀律且持續的練習來建立
### 個人想法與未來改進方向
- 目前網站內容偏向文字密集；未來版本可以加入**專案展示區**，連結到 Project 0 / Project B，並附上 CI 徽章與測試結果範例
- 加入**深色／淺色主題切換**，提升不同瀏覽環境下的舒適度
- 加入**動態時間軸／近況區塊**，整理近期課程進度與 commit 紀錄，讓訪客能看到持續的進展，而不只是靜態的快照
- 為技術背景區塊加入小型 **CSS grid 排版**，隨著技能清單增加時能更好地擴充
---
 
## 2. 課程成果與學習紀錄
 
### 我完成了什麼
| 產出 | 說明 | 連結 |
|-------------|-------------|------|
| Project 0 | Two Sum — 兩種演算法解法（O(n²) 與 O(n)）、完整測試套件、CI/CD，以及 Docker 容器化 | [→ Repo](https://github.com/Cyanlit/11402_CS351_Project0) |
| Project B | CSV 迷你資料庫與查詢引擎 — 透過 CLI 載入、建立索引並查詢 CSV 資料 | [→ Repo](https://github.com/Cyanlit/11402_CS351_ProjectB) |
| Portfolio | 部署於 GitHub Pages 的極簡個人簡介網站 | [→ Site](https://cyanlit.github.io/) |
 
### 重要學習里程碑
- **兩種演算法的對照** — 同時實作暴力解與基於雜湊表的解法，直接對比 O(n²) 與 O(n) 的行為差異
- **結構化的專案文件** — Project 0 包含一整套依循軟體工程慣例的 `docs/` 文件（用途定義、規劃、SRS、SDS、測試計畫、驗收測試、追溯矩陣、部署指南、已知問題）
- **使用 GitHub Actions 的 CI/CD** — 設定了能在每次 push 與 pull request 時自動建置 C++ 專案並執行測試套件的工作流程
- **使用 Docker 進行容器化** — 撰寫 `Dockerfile`，使建置與測試流程能在容器中重現，不受主機環境影響
- **AI 使用透明化** — Project 0 透過獨立的 `AI_POLICY.md` 與 `AI_USAGE.md` 文件，明確記錄 AI 的參與方式
### 學習反思
 
在這門課之前，我使用 Git 的方式相當基礎——大多只是把完成的程式碼推上去，幾乎沒有結構或文件可言。CS351 大幅改變了這一點。
 
特別是在 Project 0 中，我並沒有只是寫完演算法就結束。我建立了一整套文件（SRS、SDS、測試計畫、驗收測試、追溯矩陣），盡量貼近真實小型軟體專案在規格訂定與驗證上的做法。這讓我不再只把問題想成「寫一個解 Two Sum 的函式」，而是當成一個包含需求、設計決策、測試涵蓋範圍與部署考量的小型系統。
 
在這個過程中與 AI 工具合作，讓我體會到：**AI 協助的成效，與我能多清楚地描述問題成正比**。當我提供精確的規格——確切的函式簽名、複雜度要求、具體的測試類別——產出的程式碼與文件需要修正的地方就少很多；相反地，如果問題描述得很模糊，結果就需要更多調整。
 
---
 
## 3. Project 0 — Two Sum
 
**Repo：** https://github.com/Cyanlit/11402_CS351_Project0
 
### 問題描述
 
給定一個整數陣列 `nums` 與一個整數 `target`，回傳兩個數字相加等於 `target` 的索引。
 
**前提假設：**
- 每組輸入恰好有一組解
- 不能重複使用同一個元素
- 回傳順序不限
**範例：**
```
Input: nums = [2, 7, 11, 15], target = 9
Output: [0, 1]
Explanation: nums[0] + nums[1] == 2 + 7 == 9
```
 
### 演算法構想
 
要求實作兩種獨立解法，皆以 `std::vector<int>` 作為輸入與輸出：
 
| 函式 | 做法 | 時間複雜度 |
|----------|----------|------------------|
| `TwoSumArray` | 使用兩層巢狀迴圈，逐一檢查每一對元素 | O(n²) |
| `TwoSumHashTable` | 使用 STL 雜湊表（`unordered_map`）單次掃描，邊掃邊記錄已出現過的值與其索引 | O(n) |
 
雜湊表解法以少量額外記憶體換取執行時間的大幅下降，當輸入規模變大時這個差異會越來越明顯——是時間／空間取捨的具體例子。
 
### 儲存庫結構
 
```
.
├── docs/                          # 完整的軟體文件集
│   ├── 00_intended_use.md        # 問題定義與範圍
│   ├── 01_plan.md                # 專案規劃
│   ├── 02_SRS.md                 # 軟體需求規格
│   ├── 03_SDS.md                 # 軟體設計規格
│   ├── 04_test_plan.md           # 測試策略
│   ├── 05_acceptance_tests.md    # 驗收標準
│   ├── 06_traceability.md        # 需求追溯矩陣
│   ├── 07_deploy.md              # 部署指南
│   └── 08_known_issues.md        # 已知限制
├── src/                           # 原始碼（TwoSumArray、TwoSumHashTable）
├── include/                       # 標頭檔
├── test/                          # 測試檔案
├── .github/workflows/             # GitHub Actions CI 設定
├── Dockerfile                     # 容器建置定義
├── CHANGELOG.md                   # 版本紀錄
├── AI_POLICY.md                   # 此專案的 AI 使用政策
├── AI_USAGE.md                    # AI 產出內容的紀錄文件
└── README.md                      # 專案總覽
```
 
### 開發過程
 
1. **先定義範圍** — 在動手寫任何程式碼之前，先與 AI 一起草擬 `00_intended_use.md` 與 `01_plan.md`，釐清這次作業中「Two Sum」的確切意涵（輸入格式、輸出格式、需要支援的邊界情況）
2. **撰寫 SRS 與 SDS** — 將非正式的問題描述轉化為正式需求（`02_SRS.md`），以及涵蓋陣列法與雜湊表法兩種做法的設計文件（`03_SDS.md`）
3. **實作兩種解法** — `TwoSumArray`（O(n²)）與 `TwoSumHashTable`（O(n)），皆接受 `std::vector<int>` 與目標值，並回傳 `std::vector<int>` 形式的索引
4. **建立測試套件** — 依照 `04_test_plan.md` 與 `05_acceptance_tests.md` 的規劃，涵蓋基本範例、負數、重複值、答案包含零，以及最小／小型輸入規模
5. **設定 CI/CD** — 撰寫 GitHub Actions 工作流程（`.github/workflows/`），在每次 `push` 與 `pull_request` 時自動觸發，建置專案並執行完整測試套件
6. **將建置容器化** — 撰寫 `Dockerfile`，讓專案可以透過以下方式建置與測試：
   ```bash
   docker build -t twosum .
   docker run twosum
   ```
7. **記錄 AI 參與情況** — 維護 `AI_POLICY.md`（此專案中 AI 的使用方式與限制）以及 `AI_USAGE.md`（記錄哪些內容實際由 AI 產生、哪些為自行撰寫）
### 本機建置
 
```bash
# 複製儲存庫
git clone https://github.com/Cyanlit/11402_CS351_Project0.git
cd 11402_CS351_Project0
 
# 建置專案
cd src
g++ -std=c++17 -o twosum main.cpp twosum.cpp
 
# 執行測試
./twosum
```
 
### 開發歷程
 
- **共 27 次 commit**，大致依循：建立骨架 → 核心演算法實作 → 測試套件 → CI/CD 設定 → Docker 容器化 → 文件補充與整理
- 全程在 **`main`** 分支上進行整合
- `docs/` 資料夾隨著程式開發逐步建立，而非事後補寫
### 測試結果
 
- 測試套件涵蓋：標準範例、負數輸入、重複值、答案包含零的情況，以及最小規模陣列
- 所有測試在每次 push 與 pull request 時透過 GitHub Actions 自動執行：
```
push / pull_request
      │
      ▼
  build (g++ / CMake)
      │
      ▼
  run test suite
      │
   ✅ pass → CI green
   ❌ fail → CI red
```
 
### 專案狀態
 
- ✅ 核心演算法已完成（`TwoSumArray`、`TwoSumHashTable`）
- ✅ 涵蓋邊界情況的完整測試套件
- ✅ GitHub Actions CI/CD
- ✅ Docker 容器化
- ✅ 完整的軟體文件集（SRS、SDS、測試計畫、追溯矩陣、部署、已知問題）
### 專案亮點
 
這個專案最有價值的部分並不是演算法本身——Two Sum 是個眾所皆知的題目——而是**圍繞著它建立起完整的文件流程**。一開始覺得為這麼小的題目寫 SRS 與 SDS 似乎有點殺雞用牛刀，但這個過程逼著我把平常憑直覺做的決定講清楚，例如「到底什麼算是邊界情況？」以及「要怎麼證明需求真的有被測試到？」（也就是追溯矩陣）。AI 在快速搭建每份文件的架構上很有幫助，但實際的技術內容——特別是需求、設計與測試之間的對應關係——還是得自己填寫並驗證。
 
---
 
## 4. Project B — CSV 迷你資料庫與查詢引擎
 
**Repo：** https://github.com/Cyanlit/11402_CS351_ProjectB
 
### 專案目標
 
在 CSV 檔案之上建立一個輕量級資料庫系統——載入一個 CSV 檔案後，讓使用者能對資料進行類似查詢的操作（篩選、排序、基本的 CRUD），概念上類似一個非常小型的 SQL 引擎。
 
### 主要功能
 
- **CSV 檔案處理** — 載入、解析並管理 CSV 檔案
- **查詢引擎** — 執行篩選、排序與操作資料列的查詢
- **命令列介面** — 提供簡單的指令來載入檔案與執行查詢
- **效能考量** — 在資料處理與檢索上以效率為設計考量
### 資料設計
 
- 輸入資料直接從 CSV 檔讀取，每一列視為一筆紀錄、每一欄視為一個欄位
- 查詢引擎針對這些紀錄運作，支援篩選式查詢（例如選出符合條件的列）以及基本的排序／操作
- 選擇使用 Pandas 處理資料、SQLite 作為後端儲存，反映出「迷你資料庫」的設計理念——快速將 CSV 資料轉換為結構化、可查詢的形式，而不是從零開始實作一套儲存引擎
### 使用方式
 
```bash
# 安裝相依套件
pip install -r requirements.txt
 
# 執行應用程式
python main.py
 
# 應用程式內的範例指令
load <filename>
query <your_query>
```
 
### 開發過程
 
1. **先確立專案目標** — 在實作之前先寫出專案概述與功能清單（CSV 處理、查詢引擎、CLI、效能），讓範圍從一開始就清楚
2. **選擇技術堆疊** — 以 Python 作為實作語言，搭配 Pandas 處理資料、SQLite 作為後端儲存，在「從零開始打造」的學習價值與實務工具之間取得平衡
3. **實作核心流程** — `load <filename>` 將 CSV 載入記憶體／資料庫，`query <your_query>` 對其執行篩選／排序操作
4. **與 AI 反覆協作** — 描述整體架構（CSV 載入 → 儲存層 → 查詢引擎 → CLI），請 AI 協助搭建各個部分的初版，再用實際的 CSV 範例檔案手動測試 CLI，確認輸出結果符合預期
### 開發歷程
 
- **共 4 次 commit**，涵蓋：初始專案設定與 README、核心 CSV 載入邏輯、查詢引擎實作，以及 CLI 整合
- 這個規模較小的專案直接在 **`main`** 分支上開發
### 專案亮點
 
這個專案與 Project 0 形成很好的對比。Project 0 著重在單一、定義明確的演算法，搭配大量文件；Project B 則著重在**將多個元件整合成一個可運作的工具**——檔案讀寫、儲存層、查詢解析器與 CLI 都必須正確協同運作。最大的收穫是：每個元件單獨「看起來沒問題」並不夠；我必須實際以真實的 CSV 範例檔案執行 `load` 再執行 `query`，才能抓到單純看程式碼不會發現的整合性問題。
 
---
 
## 5. GitHub 工作流程證據
 
### Commit 歷史
- **Project 0：** 27 次 commit — 反映從骨架建立、實作、測試、CI、Docker 到文件的完整進程
- **Project B：** 12 次 commit — 每個主要開發階段一次（設定、CSV 處理、查詢引擎、CLI）
- **個人網站：** 11 次 commit — 內容與版面的多次調整
### 分支
- 三個儲存庫目前皆使用 **`main`** 作為主要分支
- Project 0 較多的 commit 數量與獨立的 `docs/` 資料夾，反映出它是這門課中工程化程度較高的產出；Project B 則因有 Project 0的開發經驗與feature branch的使用，導致commith次數較少
- 未來可以考慮將每個重大變更拆分為 feature branch 並搭配 pull request，以更明確地展現 code review 流程
### CI/CD（Project 0）
 
`.github/workflows/` 下的 GitHub Actions 工作流程會在每次 push 與 pull request 時觸發：
 
```
push / pull_request
      │
      ▼
  build C++ project (g++ / CMake)
      │
      ▼
  run full test suite
      │
   ✅ pass → build marked successful
   ❌ fail → build marked failed
```
 
### 容器化（Project 0）
 
專案中包含 `Dockerfile`，使建置與測試環境可重現：
 
```bash
docker build -t twosum .
docker run twosum
```
 
這代表 CI 環境、評分者的機器與我自己的機器，理論上都應該得到相同的建置與測試結果。
 
---
 
## 6. AI 輔助開發反思
 
這門課中我主要使用的 AI 工具，是整合在編輯器中的 AI 程式設計助理，三項產出（個人網站、Project 0、Project B）都使用了它。
 
### 我如何與 AI 互動
 
我並沒有把 AI 當成一次性的程式碼產生器來使用，而是將它納入一個反覆迭代的循環中：
 
```
我  →  描述目標、限制條件與預期輸出
AI  →  產出程式碼、文件或設定檔草稿
我  →  建置／執行，對照規格檢查結果
我  →  「這個測試案例缺漏了」／「SRS 的這部分要修改」／「Dockerfile 需要調整」
AI  →  更新對應的檔案
我  →  重新測試，確認無誤後再 commit
```
 
這個循環在每個元件上都重複進行——演算法實作、每一份文件、CI 工作流程，以及 Dockerfile。
 
### 範例一 — Project 0 的文件集
 
我並沒有直接要求「給我一份 README」，而是分別請 AI 產出 `docs/` 資料夾中的每一份文件——先是用途定義，再來是 SRS、SDS、測試計畫，依此類推。一份一份來、並讓前一份文件作為下一份的脈絡，產出的文件之間遠比一次要求整套文件來得一致且可追溯。之後我再逐一檢視每份文件，自行修正其中的技術細節（例如確切的複雜度說明、確切的測試案例描述）。
 
### 範例二 — Project 0 的演算法
 
針對 `TwoSumArray` 與 `TwoSumHashTable`，我明確指定了函式簽名（`std::vector<int>` 輸入輸出）與要求的複雜度（分別為 O(n²) 與 O(n)），請 AI 實作兩種版本。接著我問了一句：*「這些實作的測試套件應該涵蓋哪些邊界情況？」*——AI 列出了重複值、答案包含零等我原本沒特別考慮到的情況；我確認這些案例合理後，再請 AI 撰寫對應的測試程式碼。
 
### 範例三 — Project B
 
在 Project B 中，我用使用者實際會輸入的指令（`load <filename>`、`query <your_query>`）來描述整個流程——CSV 載入、查詢引擎與 CLI。AI 一次產出了相關檔案的初版實作。由於這個專案前期的文件比 Project 0 少很多，我更依賴**以範例 CSV 檔案進行手動測試**來驗證正確性——實際執行 `load` 與 `query` 指令，並對照輸出結果是否符合預期。
 
### 哪些事情由我自己完成
 
- **決定範圍與結構** — 決定 Project 0 中 `docs/` 各份文件該包含什麼內容，以及 Project B 的最小功能集應該如何劃定
- **驗證複雜度宣稱** — 確認 `TwoSumArray` 與 `TwoSumHashTable` 的實際行為真的符合文件中所宣稱的 O(n²) 與 O(n)
- **執行並檢視測試結果** — 確認測試套件在本機與 CI 上都能通過，而不是只看 AI 產生的測試「看起來合理」就直接相信
- **commit 前的最終檢查** — 每一次 commit 所包含的程式碼與文件，都是我親自閱讀並理解過的
### 我學到的事
 
1. **文件也適合採用與程式碼相同的迭代方式撰寫。** 一次處理一份文件、並延續前一份的脈絡，比一次要求整套文件，能產出更連貫的 `docs/` 內容。
2. **複雜度與正確性的宣稱需要獨立驗證。** AI 實作出來的演算法可能「看起來」符合所宣稱的複雜度，但確認它是否真的如此、以及測試是否確實涵蓋相關情況，是我自己的責任。
3. **規模較小、範圍明確的專案（如 Project B），會將驗證的重擔轉移到手動測試上。** 在沒有完整文件／測試計畫架構的情況下，使用真實輸入檔案進行實際操作，是我發現整合性問題的主要方式。
 
