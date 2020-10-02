- Add a SignalR hub
	+ Create class extends Hub superlass
	+ Create Hub's function(s) that Clients will invoke
	+ Create Models (ChatMessage.cs, etc)
	+ Config Startup.cs (Add service and Add route)
- Build the JavaScript client:
	+ Set handler to trigger when message from the server comes (ReceiveMessage)
	+ Submit button calls sendMessage(text)
	+ sendMessage(text) validates message and calls connection.invoke('SendMessage', chatterName, text)
	+ connection.start()
- Handle hub connections events
	+ Override OnConnectedAsync and OnDisconnectedAsync

- Handle client connection events
	+ Set handlers for connect and disconnect