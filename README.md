<script src="https://unpkg.com/blip-chat-widget@1.11.*" type="text/javascript">
</script>
<script>
    (function () {
        window.onload = function () {
          var builder = new BlipChat()
            .withAppKey('YmxpcHRlc3RjYXJkczoxOGE5NzUwYS1kZjAxLTRhNTgtODA1ZC1kY2ExYmI2NTBmZjk=')
            .withButton({
              color: '#F00',
              icon:
                'https://www.google.com.br/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png',
            })
            .withAuth({
              authType: BlipChat.DEV_AUTH,
              userIdentity: '1234567',
              userPassword: 'MTIzNDU2',
            })
            .withAccount({
              fullName: 'John Doe',
              email:'johndoe@gmail.com',
              phoneNumber: '+15055034455',
              city: 'Decatur',
            })
            .withEventHandler(BlipChat.ENTER_EVENT, function () {
              console.log('enter')
            })
            .withEventHandler(BlipChat.LEAVE_EVENT, function () {
              console.log('leave')
            })
            .withEventHandler(BlipChat.LOAD_EVENT, function () {
              console.log('chat loaded')
            })
            .withEventHandler(BlipChat.CREATE_ACCOUNT_EVENT, function () {
              console.log('account created')
            })
          builder.build()
      }
    })();
</script>
