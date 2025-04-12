# CNAD Assignment 2

國立臺灣大學  
雲原生應用程式開發 (Cloud Native Application Development)  
作業二 - GitHub 協作與自動化測試實作

## 學生資訊
- **姓名**: 鄭新曄
- **學號**: R12525072

## GitHub URL
[https://github.com/Peter-Cheng028/CNAD_assignment2.git](https://github.com/Peter-Cheng028/CNAD_assignment2.git)

## 實作內容

### 1. Repository 操作
- 建立一個 Public Repository，名稱為 `CNAD_assignment2`。
- 修改並更新 `README.md` 文件內容。
- 建立兩個額外分支：
  - `hw1-p`：用於展示 GitHub Action 測試成功流程
  - `hw1-f`：用於展示 GitHub Action 測試失敗流程

### 2. Issue 建立與管理
- 建立並使用 Issue Template，確保問題回報的一致性。
- 使用 Issue Template 開立新的 Issue，驗證模板使用。
- 手動建立一般 Issue，以驗證基本 Issue 功能。

### 3. Pull Request (PR) 與留言互動
- 從 `hw1-p` 分支提交 PR 至 `main` 分支：
  - 修改檔案：`README.md` 及相關文件
  - PR 測試流程通過
- 從 `hw1-f` 分支提交 PR 至 `main` 分支：
  - 後續新增檔案：`fail.txt`，用以觸發自動化測試失敗
  - PR 測試流程失敗
- 在 PR 中針對程式碼修改進行留言討論互動。

### 4. GitHub Action 自動化測試
- 建立 GitHub Action Workflow 檔案：`.github/workflows/ci.yml`  
- 設置 Workflow，包含以下步驟：
  1. Checkout code
  2. Setup environment
  3. Code Lint Check
  4. Generate Test Report
  5. Run tests（偵測檔案 `fail.txt` 來決定測試成功或失敗）
- 驗證 Workflow 執行結果：
  - `hw1-p` 分支 PR 測試成功 (Passed)
  - `hw1-f` 分支 PR 測試失敗 (Failed)

