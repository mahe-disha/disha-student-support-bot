<!DOCTYPE html>
<html>
  <head>
    <title>Disha Student Support</title>
  </head>
  <body>
    <!-- Your website content here -->

    <!-- Watson Assistant Chatbot Script -->
    <script>
      window.watsonAssistantChatOptions = {
        integrationID: "e92f3811-9941-4832-93ec-83c8f39e0d64",
        region: "au-syd",
        serviceInstanceID: "43acaeee-2670-4736-941d-81536ad93753",
        onLoad: async (instance) => { await instance.render(); }
      };
      setTimeout(function(){
        const t=document.createElement('script');
        t.src="https://web-chat.global.assistant.watson.appdomain.cloud/versions/" + 
              (window.watsonAssistantChatOptions.clientVersion || 'latest') + "/WatsonAssistantChatEntry.js";
        document.head.appendChild(t);
      });
    </script>
  </body>
</html>
