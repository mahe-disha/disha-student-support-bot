<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Disha Student Help Desk</title>
  <style>
    body {
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #f8f9fa, #e0f7fa);
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    header {
      background-color: #00695c;
      color: white;
      padding: 1.5rem;
      width: 100%;
      text-align: center;
      font-size: 1.8rem;
      font-weight: bold;
    }

    .container {
      margin: 2rem;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
      width: 90%;
      max-width: 1000px;
    }

    button {
      background-color: #004d40;
      color: white;
      padding: 1.2rem;
      border: none;
      border-radius: 12px;
      font-size: 1rem;
      box-shadow: 2px 4px 10px rgba(0,0,0,0.2);
      cursor: pointer;
      transition: all 0.3s ease-in-out;
    }

    button:hover {
      background-color: #00796b;
      transform: scale(1.05);
    }

    footer {
      margin-top: 3rem;
      padding: 1rem;
      font-size: 0.9rem;
      color: #555;
    }

    .chat-button {
      margin-top: 2rem;
      background-color: #00796b;
      font-size: 1.1rem;
    }
  </style>
</head>
<body>

  <header>Disha Student Help Desk</header>

  <div class="container">
    <button onclick="alert('Faculty contact: faculty@college.edu, Ph: 1234567890')">📞 Faculty Contact Info</button>
    <button onclick="alert('College Timing: 9 AM to 5 PM')">⏰ College Timing</button>
    <button onclick="alert('Library Info: Open 8 AM – 8 PM, Contact: library@college.edu')">📚 Library Info</button>
    <button onclick="alert('Placement: placement@college.edu, Ph: 9876543210')">💼 Placement Cell</button>
    <button onclick="alert('Courses Offered: B.Tech, M.Tech, MBA, etc.')">📖 Course Info</button>
    <button onclick="alert('Fees: Visit college.edu/fees for details')">💰 Fees Details</button>
    <button onclick="alert('Clubs: Music, Dance, Drama, Tech Club')">🎭 Extracurricular Activities</button>
  </div>

  <button class="chat-button" onclick="openChatbot()">💬 Open Disha Chatbot</button>

  <footer>Powered by Disha Chatbot & IBM Watson Assistant</footer>

  <!-- IBM Watson Assistant Chatbot Script -->
  <script>
    window.watsonAssistantChatOptions = {
      integrationID: "e92f3811-9941-4832-93ec-83c8f39e0d64", // Your Integration ID
      region: "au-syd", // Your region
      serviceInstanceID: "43acaeee-2670-4736-941d-81536ad93753", // Your instance ID
      onLoad: async (instance) => {
        window.ibmWatsonAssistantChatInstance = instance;
        await instance.render();
      }
    };
    setTimeout(function(){
      const t = document.createElement('script');
      t.src = "https://web-chat.global.assistant.watson.appdomain.cloud/versions/" +
              (window.watsonAssistantChatOptions.clientVersion || 'latest') +
              "/WatsonAssistantChatEntry.js";
      document.head.appendChild(t);
    }, 0);
  </script>

  <!-- Script to Manually Open Chatbot -->
  <script>
    function openChatbot() {
      if (window.ibmWatsonAssistantChatInstance) {
        window.ibmWatsonAssistantChatInstance.openWindow();
      } else {
        alert("Chatbot is still loading. Please wait a few seconds.");
      }
    }
  </script>

</body>
</html>
