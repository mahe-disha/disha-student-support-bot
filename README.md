<script>
  window.watsonAssistantChatOptions = {
    integrationID: "e92f3811-9941-4832-93ec-83c8f39e0d64", // The ID of this integration.
    region: "au-syd", // The region your integration is hosted in.
    serviceInstanceID: "43acaeee-2670-4736-941d-81536ad93753", // The ID of your service instance.
    onLoad: async (instance) => { await instance.render(); }
  };
  setTimeout(function(){
    const t=document.createElement('script');
    t.src="https://web-chat.global.assistant.watson.appdomain.cloud/versions/" + (window.watsonAssistantChatOptions.clientVersion || 'latest') + "/WatsonAssistantChatEntry.js";
    document.head.appendChild(t);
  });
</script># disha-student-support-bot
first chatbot
