client.on('ready', () => {
    console.log(`Bot is ON, with ${client.users.cache.size} users and ${client.guilds.cache.size} servers.`); 
      let activities = [
        `⚙️ by suizzz ⚙️`,
          `🌎 TESTES 🌎 `,
          `🧸 by suizzz 🧸`,
          `🌎 TESTES 🌎`
        ],
        i = 0;
      setInterval( () => client.user.setActivity(`${activities[i++ % activities.length]}`, {
            type: "WATCHING"
          }), 1000 * 10); 
      client.user
          .setStatus("dnd")
          .catch(console.error);
    });
