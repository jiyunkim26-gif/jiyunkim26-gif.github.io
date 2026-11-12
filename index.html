<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>전용 폴더 바로가기</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      background: #f1f3f5;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 20px;
    }
    .card {
      background: #ffffff;
      width: 100%;
      max-width: 420px;
      padding: 36px 28px;
      border-radius: 16px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.06);
      text-align: center;
    }
    h2 { font-size: 22px; color: #212529; margin-bottom: 8px; }
    p { font-size: 14px; color: #868e96; margin-bottom: 24px; line-height: 1.5; }
    .input-group { display: flex; flex-direction: column; gap: 10px; }
    input {
      width: 100%;
      padding: 14px;
      font-size: 16px;
      border: 1.5px solid #dee2e6;
      border-radius: 8px;
      outline: none;
      transition: border-color 0.2s;
    }
    input:focus { border-color: #1a73e8; }
    button {
      width: 100%;
      padding: 14px;
      font-size: 16px;
      font-weight: 600;
      color: #fff;
      background: #1a73e8;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.2s;
    }
    button:hover { background: #1557b0; }
    #msg {
      margin-top: 16px;
      font-size: 14px;
      min-height: 20px;
      color: #e03131;
    }
  </style>
</head>
<body>

  <div class="card">
    <h2>전용 폴더 조회</h2>
    <p>배정된 식별 코드(또는 이름/전화번호)를 입력하세요.</p>
    
    <div class="input-group">
      <input type="text" id="userInput" placeholder="식별값 입력" autocomplete="off" onkeypress="if(event.key === 'Enter') checkAndRedirect()">
      <button onclick="checkAndRedirect()" id="submitBtn">폴더로 이동하기</button>
    </div>

    <div id="msg"></div>
  </div>

  <script>
    // ==========================================
    // [데이터 매핑 설정]
    // 키: 사용자 입력값의 SHA-256 해시값 (소문자)
    // 값: 이동할 구글 드라이브 폴더 전체 URL
    // ==========================================
    const FOLDER_MAP = {
      // 예시 1: 입력값 "1234"
      "03ac674216f3e15c761ee1a5e255f067953623c8b388b4459e13f978d7c846f4": "https://drive.google.com/drive/folders/폴더ID_1",

      // 예시 2: 입력값 "홍길동"
      "60c6d7a46cbe702a4358a98f1ec1ea3b719cb3da101fa2eb05b76cf6b1424e88": "https://drive.google.com/drive/folders/폴더ID_2"
    };

    // 브라우저 기본 내장 Web Crypto API로 SHA-256 해시 계산
    async function getSHA256(str) {
      const buffer = new TextEncoder().encode(str.trim().toLowerCase());
      const hashBuffer = await crypto.subtle.digest("SHA-256", buffer);
      return Array.from(new Uint8Array(hashBuffer))
        .map(b => b.toString(16).padStart(2, '0'))
        .join('');
    }

    async function checkAndRedirect() {
      const input = document.getElementById("userInput").value;
      const msg = document.getElementById("msg");
      const btn = document.getElementById("submitBtn");

      msg.innerText = "";
      if (!input.trim()) {
        msg.innerText = "식별값을 입력해 주세요.";
        return;
      }

      btn.innerText = "확인 중...";
      btn.disabled = true;

      try {
        const hash = await getSHA256(input);
        const folderUrl = FOLDER_MAP[hash];

        if (folderUrl) {
          // 본인 폴더로 즉시 이동
          window.location.href = folderUrl;
        } else {
          msg.innerText = "일치하는 전용 폴더가 없습니다.";
          btn.innerText = "폴더로 이동하기";
          btn.disabled = false;
        }
      } catch (e) {
        msg.innerText = "처리 중 오류가 발생했습니다.";
        btn.innerText = "폴더로 이동하기";
        btn.disabled = false;
      }
    }
  </script>
</body>
</html>
