<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8" />
  <title>دردشة AI - تجربة محلية</title>
  <style>
    body{font-family:Tahoma, Arial, sans-serif;background:#f4f7fb;padding:18px;color:#0b1220}
    .wrap{max-width:760px;margin:12px auto}
    h1{margin:0 0 10px}
    #chat{background:#fff;border-radius:10px;padding:12px;height:420px;overflow:auto;border:1px solid #e6eefc}
    .msg{margin:8px 0;padding:10px;border-radius:8px;max-width:80%}
    .user{background:#0b75ef;color:#fff;margin-left:auto;text-align:left;border-bottom-right-radius:2px}
    .bot{background:#eef3ff;color:#0b1220;margin-right:auto;text-align:right;border-bottom-left-radius:2px}
    .controls{display:flex;gap:8px;margin-top:10px}
    input{flex:1;padding:10px;border-radius:8px;border:1px solid #d6e4ff}
    button{padding:10px 14px;border-radius:8px;border:none;background:#0b6ef0;color:#fff;cursor:pointer}
    .small{font-size:13px;color:#667085;margin-top:8px}
  </style>
</head>
<body>
  <div class="wrap">
    <h1>دردشة الذكاء الاصطناعي — تجربة محلية</h1>
    <div class="small">ملاحظة: هذا الملف يحتوي طلبات مباشرة إلى OpenAI — آمن فقط إذا شغّلته على جهازك ولم ترفعه إلى أي مكان.</div>

    <div id="chat" aria-live="polite"></div>

    <div class="controls">
      <input id="input" placeholder="اكتب سؤالك..." />
      <button id="send">إرسال</button>
    </div>

    <div style="margin-top:10px" class="small">لو ظهر خطأ CORS شغّل صفحة الواجهة عبر سيرفر محلي (مثلاً: <code>python -m http.server 8080</code> ثم افتح http://localhost:8080/index_local_key.html).</div>
  </div>

  <script>
    // ======== ضع مفتاحك هنا ========
    const API_KEY = "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";
    // ===============================

    const chat = document.getElementById('chat');
    const input = document.getElementById('input');
    const send = document.getElementById('send');

    function append(text, cls){
      const d = document.createElement('div');
      d.className = 'msg ' + cls;
      d.textContent = text;
      chat.appendChild(d);
      chat.scrollTop = chat.scrollHeight;
    }

    async function sendMessage(){
      const text = input.value.trim();
      if(!text) return;
      append(text, 'user');
      input.value = '';

      append('جاري الرد...', 'bot');

      try {
        const resp = await fetch("https://api.openai.com/v1/chat/completions", {
          method: "POST",
          headers: {
            "Content-Type": "application/json",
            "Authorization": `Bearer ${API_KEY}`
          },
          body: JSON.stringify({
            model: "gpt-3.5-turbo",
            messages: [{ role: "user", content: text }],
            max_tokens: 500,
            temperature: 0.7
          })
        });

        const data = await resp.json();
        // إزالة رسالة "جاري الرد..."
        const last = chat.querySelectorAll('.bot');
        if(last.length) last[last.length-1].remove();

        if(resp.ok && data.choices && data.choices[0] && data.choices[0].message){
          append(data.choices[0].message.content.trim(), 'bot');
        } else {
          append('لم يصل رد من الخادم. تحقق من المفتاح أو الرسائل في الكونسول.', 'bot');
          console.error(data);
        }
      } catch (err) {
        // إزالة رسالة "جاري الرد..."
        const last = chat.querySelectorAll('.bot');
        if(last.length) last[last.length-1].remove();

        append('حدث خطأ: ' + (err.message || err), 'bot');
        console.error(err);
      }
    }

    send.addEventListener('click', sendMessage);
    input.addEventListener('keydown', (e)=>{ if(e.key === 'Enter') sendMessage(); });

    // رسالة ترحيب
    append('مرحبا! ابدأ بكتابة سؤالك.', 'bot');
  </script>
</body>
</html>
