### Hi there 👋

<!--
**mikaelprogramador/mikaelprogramador** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
 name: gitartwork from a contribution graph
 on: 
   push:
   schedule:
     - cron: '* */24 * * *'
   workflow_dispatch:
 jobs:
   build:
     name: Make gitartwork SVG
     runs-on: ubuntu-latest
     steps:
       - uses: actions/checkout@v2
       - uses: jasineri/gitartwork@v1
         with:
            # Use this username's contribution graph  
            user_name: jasineri
            # Text on contribution graph 
            text: MIKAEL
       - uses: jasineri/simple-push-action@v1
