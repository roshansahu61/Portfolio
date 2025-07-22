<template>
  <div class="chat-container">
    <div class="chat-header">💬 Chat with Roshan AI</div>
    <div class="chat-messages" ref="chatMessages">
      <div v-for="(msg, index) in messages" :key="index" :class="msg.sender">
        <strong>{{ msg.sender === 'user' ? 'You' : 'Roshan AI' }}:</strong> {{ msg.text }}
      </div>
    </div>
    <div class="chat-input">
      <input
        v-model="input"
        @keyup.enter="sendMessage"
        placeholder="Type your message..."
      />
      <button @click="sendMessage">Send</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "RoshanChatbot",
  data() {
    return {
      input: "",
      messages: [],
    };
  },
  methods: {
    sendMessage() {
      const text = this.input.trim();
      if (!text) return;

      this.messages.push({ sender: "user", text });

      // Simulate bot response after 500ms
      setTimeout(() => {
        const reply = this.generateReply(text);
        this.messages.push({ sender: "bot", text: reply });

        // Auto-scroll to bottom
        this.$nextTick(() => {
          const el = this.$refs.chatMessages;
          el.scrollTop = el.scrollHeight;
        });
      }, 500);

      this.input = "";
    },
    generateReply(text) {
      const lower = text.toLowerCase();
      if (lower.includes("hello")) return "Hi there! I'm Roshan AI. 😊";
      if (lower.includes("help")) return "I'm here to help! What do you need?";
      if (lower.includes("who are you")) return "I'm Roshan AI, your personal assistant.";
      return "Sorry, I didn’t understand that. Can you rephrase?";
    },
  },
};
</script>

<style scoped>
.chat-container {
  width: 350px;
  max-height: 500px;
  margin: 30px auto;
  border: 2px solid #ddd;
  border-radius: 10px;
  overflow: hidden;
  background: #fff;
  display: flex;
  flex-direction: column;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}
.chat-header {
  background-color: #0D1117;
  color: white;
  padding: 10px;
  font-weight: bold;
  text-align: center;
}
.chat-messages {
  flex: 1;
  padding: 10px;
  overflow-y: auto;
  background-color: #f9f9f9;
}
.chat-input {
  display: flex;
  border-top: 1px solid #ccc;
}
.chat-input input {
  flex: 1;
  border: none;
  padding: 10px;
  font-size: 14px;
}
.chat-input button {
  background-color: #0D1117;
  color: white;
  border: none;
  padding: 10px 15px;
  cursor: pointer;
}
.user {
  text-align: right;
  color: blue;
  margin-bottom: 8px;
}
.bot {
  text-align: left;
  color: green;
  margin-bottom: 8px;
}
</style>
