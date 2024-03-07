# MISHU Embed 🌐

Welcome to the **MISHU Embed** project! This project is focused on customizing the chatbot experience to match the MISHU brand, removing Flowise branding, and making the chat interface more personalized and engaging for users.

## Objective 🎯

1. **Remove Flowise Branding:** Transition from Flowise to MISHU branding.
2. **Change to MISHU Branding:** Implement MISHU's visual identity across the chatbot.
3. **Change Starting Message:** Update the chatbot's greeting to better align with Agent Maya's voice.
4. **Add Avatar Picture and Name:** Introduce a more personable chatbot experience with an avatar.
5. **Change Color Scheme:** Update the color palette to match MISHU's branding.

## Implementation Details 🛠️

### Embed Pop-Up HTML

To integrate the MISHU chatbot into your website, include the following script in your HTML. This script initializes the chatbot with MISHU branding, a custom starting message, an avatar picture, and updates the color scheme.

```html
<script type="module">
  import Chatbot from 'https://cdn.jsdelivr.net/gh/blqsMISHU/mishuembed/dist/web.js';

  // Generate a unique session ID with the current timestamp for uniqueness
  const sessionIdPrefix = "WEB";
  const sessionId = `${sessionIdPrefix}`;

  Chatbot.init({
    chatflowid: "810011a1-bfa7-4f14-8110-4a9a8964c449",
    apiHost: "https://mishuai-mishu.hf.space",
    theme: {
      button: {
        backgroundColor: '#48c3db',
        right: 20,
        bottom: 20,
        size: 'medium',
        iconColor: 'white',
      },
      chatWindow: {
        showTitle: true,
        title: 'Maya',
        titleAvatarSrc: 'https://raw.githubusercontent.com/blqsMISHU/mishuembed/main/DALL%C2%B7E%202024-02-20%2010.20.10%20-%20Create%20a%20photo-realistic%20image%20of%20a%20friendly%20and%20approachable%2040-year-old%20Asian%20female%20with%20a%20blend%20of%20Chinese%20and%20Malay%20features.%20She%20embodies%20a%20pret.webp',
        welcomeMessage: 'Hello! 👋 I am Maya, a Business Consultant at MISHU. How can I assist you today?',
        backgroundColor: '#ffffff',
        height: 700,
        width: 400,
        fontSize: 16,
        botMessage: {
          backgroundColor: '#48c3db',
          textColor: '#ffffff',
          showAvatar: true,
          avatarSrc: 'https://raw.githubusercontent.com/blqsMISHU/mishuembed/main/DALL%C2%B7E%202024-02-20%2010.20.10%20-%20Create%20a%20photo-realistic%20image%20of%20a%20friendly%20and%20approachable%2040-year-old%20Asian%20female%20with%20a%20blend%20of%20Chinese%20and%20Malay%20features.%20She%20embodies%20a%20pret.webp',
        },
        userMessage: {
          backgroundColor: '#48c3db',
          showAvatar: true,
          avatarSrc: 'https://raw.githubusercontent.com/blqsMISHU/mishuembed/main/icons8-user-90.svg',
        },
        textInput: {
          sendButtonColor: '#29A2BA',
        },
      },
    },
    chatflowConfig: {
      sessionId: sessionId
    },
  });
</script>




