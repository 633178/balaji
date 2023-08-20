<!DOCTYPE html>
<html>
<head>
  <title>Chat with Friends</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <div id="chat-container">
    <div id="chat-messages"></div>
    <input type="text" id="message-input" placeholder="Type your message...">
    <button id="send-button">Send</button>
  </div>

<style>
#chat-container {
  width: 400px;
  margin: 0 auto;
}

#chat-messages {
  height: 300px;
  border: 1px solid #ccc;
  padding: 10px;
  overflow-y: scroll;
}

#messa
  width: 300px;
  padding: 5px;
}

#send-button {
  padding: 5px 10px;
} 
</style>
<script>
document.addEventListener('DOMContentLoaded', function() {
  var messageInput = document.getElementById('message-input');
  var sendButton = document.getElementById('send-button');
  var chatMessages = document.getElementById('chat-messages');

  sendButton.addEventListener('click', function() {
    var message = messageInput.value.trim();
    if (message !== '') {
      var messageElement = document.createElement('p');
      messageElement.textContent = message;
      chatMessages.appendChild(messageElement);
      messageInput.value = '';
    }
  });

  messageInput.addEventListener('keydown', function(event) {
    if (event.keyCode === 13) { // Enter key
      sendButton.click();
    }
  });
});</script>
</body>
</html>
