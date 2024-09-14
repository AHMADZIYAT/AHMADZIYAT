<script src="https://unpkg.com/blip-chat-widget@1.11.*" type="text/javascript"></script>
<script>
    (function () {
        window.onload = function () {
          var blipClient = new BlipChat()
          .withAppKey('YOUR-APP-KEY')
          .withEventHandler(BlipChat.CREATE_ACCOUNT_EVENT, function () {
              blipClient.sendMessage({
                  "type": "text/plain",
                  "content": "Start"
              });
          });
          blipClient.build();
        }
    })();
</script>
