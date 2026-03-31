# 🌐 自定義網路檢索 (Custom Web Search)
LangBot_plug-in-Custom-Web-Search-

為 LangBot 的本地大語言模型 (LLM) 而服務的網絡檢索之插件！  
本插件允許 AI 透過你指定的搜尋引擎，獲取即時的網路資訊，突破模型訓練資料的時效限制。

---

## ✨ 核心特色
- **100% 免費，無需 API Key**  
  不同於 Google API 或 Tavily 需要付費或申請密鑰，本插件透過模擬瀏覽器直接抓取網頁純文字，開箱即用！
- **高度客製化**  
  你可以將搜尋來源設定為 Google、Bing、B站、維基百科，甚至是你們公司的內部搜尋系統！（但是容易遇到阻擋）
- **輕量且安全**  
  自動過濾網頁中的腳本 (JS) 與樣式 (CSS)，只將乾淨的純文字餵給 AI，節省 Token 消耗。

---

## ⚙️ 如何配置 (配置指南)
1. 安裝插件後，請進入 LangBot 後台的「插件擴展」點擊已安裝，點擊這個插件。  
2. 你必須在「搜尋引擎網址」欄位中填寫一個帶有 `{query}` 佔位符的網址。  
3. 當 AI 想要搜尋時，它會自動將 `{query}` 替換為實際的搜尋關鍵字。  

---

## 📋 常用搜尋引擎配置參考

| 搜尋引擎 | 穩定度 | 配置網址填寫方式 |
|----------|--------|------------------|
| DuckDuckGo (預設/推薦) | ⭐⭐⭐⭐⭐ | https://html.duckduckgo.com/html/?q={query} |
| 維基百科 (推薦) | ⭐⭐⭐⭐⭐ | https://zh.wikipedia.org/w/index.php?search={query} |
| Bilibili (小概率卡殼) | ⭐⭐⭐⭐⭐ | https://search.bilibili.com/all?keyword={query} |
| 百度 (容易吃到廣告) | ⭐⭐⭐ | https://www.baidu.com/s?wd={query} |
| Bing (容易遇到驗證碼) | ⭐⭐ | https://www.bing.com/search?q={query} |
| Google (易被阻擋) | ⭐ | https://www.google.com/search?q={query} |

---

## 🔍 測試範例

### 測試於 B站之檢索
<img width="613" height="179" alt="image" src="https://github.com/user-attachments/assets/ccdb970f-5123-4d58-9790-00e23e2822e7" />

### 測試於 Wiki 之檢索
<img width="610" height="204" alt="image" src="https://github.com/user-attachments/assets/053c040f-d222-45bf-9ebe-3ee6f5da20c4" />

---

## 💡 Pro Tip
強烈建議使用預設的 **DuckDuckGo HTML 版**。  
由於本插件是透過直接抓取網頁內容來運作，Google 等大型搜尋引擎可能會攔截非瀏覽器的自動化請求 (跳出 CAPTCHA 驗證碼)，導致 AI 無法獲取內容。

---

## 🤖 觸發方式
在工作流中將本插件的工具 (Tool) 授權給機器人後，你可以直接問機器人：

- 「幫我搜尋一下最新的 iPhone 17 消息」  
- 「今天基隆的天氣如何？」  
- 「總結一下最近的熱門新聞」  

AI 會自動判斷是否需要上網查資料，並呼叫本插件返回最新結果！
