# AI 協作全域引導：Falsiluna (ArcaneGenesis)

## 1. 技術棧與核心設定 (Stack & Settings)
- **引擎與語言：** Unity (Unity 遊戲引擎) 2D 專案 / C# (C# 程式語言)。
- **核心組件：** 新版 Input System (輸入系統)、LDTK (LDTK 地圖編輯器) 導出、ZeroFriction (無摩擦力 2D 物理材質)。
- **視角與風格：** 類惡魔城橫卷軸、黑暗環境敘事、高精密角色控制。

## 2. 代碼架構與命名規範 (Code Architecture)
- **腳本根目錄：** `Assets/_Games/Scripts/`
- **文字化編程規範：**
  - 每個 Script (腳本) 頂部必須以註解條列其 Import (呼叫/依賴) 的其他內部腳本。
  - 每個 Function (函式) 上方必須註解其職責。
  - 呼叫外部 Function (函式) 或第三方 API (應用程式介面) 時，需在行末註解註明來源檔案、預期行為與行數。
- **核心命名路徑：**
  - 玩家控制：`Player/` -> `PlayerController.cs` (核心控制), `EnergySystem.cs` (能量), `LightBallController.cs` (光球)
  - 戰鬥與生命：`Combat/` -> `HealthSystem.cs` (通用生命管理), `DamageTrap.cs` (傷害陷阱)
  - UI 系統：`UI/` -> `PlayerUIController.cs` (UI 控制)

## 3. 當前開發階段 (Current Phase)
- **當前重點：** [階段2] 玩家系統完善（攻擊系統、動作擴充、生命值系統整合）。
- **當前任務：** 處理玩家死亡演出、狀態凍結、重生邏輯，以及判定與特定物件的交互。

## 4. AI 輸出嚴格限制 (AI Constraints)
- **格式：** 嚴禁任何前言與後語，直接給出目標程式碼或解決方案。
- **註解要求：** 所有原理說明、潛在風險（如 NullReferenceException (空值引用例外)、效能瓶頸）、API (應用程式介面) 原理，必須「全部」寫在程式碼區塊內的註解中。
- **資訊不足：** 若資訊不足以給出 100% 正確的代碼，必須立刻停止生成並列出提問清單。