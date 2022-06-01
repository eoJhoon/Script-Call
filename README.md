# Script-Call



//autor:eoJhoon

const { joinVoiceChannel } = require('@discordjs/voice');

client.on("ready", () => {

    let channel = client.channels.cache.get("981319850532155454"); //botar id do canal de voz 

    joinVoiceChannel({
        channelId: channel.id,
        guildId: channel.guild.id,
        adapterCreator: channel.guild.voiceAdapterCreator,
    })

    console.log("Entrei no canal de voz eojhoon [" + channel.name + "] com sucesso.") //se quiser pode mudar 
});

client.on("messageCreate", (mesasge) => {

    let channel = client.channels.cache.get("981319850532155454"); // botar id do canal de voz

    joinVoiceChannel({
        channelId: channel.id,
        guildId: channel.guild.id,
        adapterCreator: channel.guild.voiceAdapterCreator,
    })
