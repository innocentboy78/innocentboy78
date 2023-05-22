- 👋 Hi, I’m @i me ...

<!---
innocentboy78/innocentboy78 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
const { Function, getBuffer } = require('../lib/')

const { generateWAMessage, proto } = require('@adiwajshing/baileys');

const image = 'https://i.imgur.com/AXtC7iH.jpeg' //MAIN IMAGE URL HERE

const logo = 'https://i.imgur.com/DkVo4Kg.jpeg'

Function(

{

pattern: 'intro ?(.)',

fromMe: true,

desc: 'Shows Me',

type: 'misc',

}, async (message, match) => {

const jid = message.jid

const number = message.client.user.jid

const thumb = await getBuffer(image)

const thumbnail = await getBuffer(logo)

const options = {}

options.contextInfo = {

forwardingScore: 999, // change it to 999 for many times forwarded

isForwarded: false,

}

// ADDED / TO REMOVE LINK PREVIEW TYPE

options.linkPreview = {

renderLargerThumbnail: true,

showAdAttribution: true,

title: "﻿࿐⋆",

body: "ᴄʟɪᴄᴋ ʜᴇʀᴇ butterfly !!",

mediaType: 1,

thumbnail: thumb,

sourceUrl: "http://wa.me/923477099576?text=_៚ʜᴇʟʟᴏ+✧⃟≼☛⃟≛⃝🇵🇰⍮⍪✗_ᷝ_ᷠ_ᷠ_ⷪ_ⷭ₅ⷷ₇ᷠ₆ⷮ𓃮 ҈⃢🎭᭄≽⃟✧+ʙɪɢ+ғᴀɴ+ᴠʀᴏ+magic_wand_"

}

// ADDED */ TO REMOVE LINK PREVIEW TYPE

options.quoted = {

key: {

fromMe: false,

participant: "0@s.whatsapp.net",

remoteJid: "status@broadcast"

},

message: {

'contactMessage': {

'displayName': ${message.pushName}, //ADD ${message.client.user.name} TO DISPLAY CLIENT USER NAME.

'vcard': BEGIN:VCARD\nVERSION:3.0\nN:XL;${message.client.user.name},;;;\nFN:${message.client.user.name},\nitem1.TEL;waid=${number.split('@')[0]}:${number.split('@')[0]}\nitem1.X-ABLabel:Ponsel\nEND:VCARD,

'jpegThumbnail': thumbnail

}

}

}

let messages = await generateWAMessage(message.jid, { text: 0ཻུ۪۪ꦽꦼ̷⸙‹•══════════════♡᭄ │       *「           」* │ *Name      :⏤͟͟͟͟͞͞͞★⃟🍒𝄞 𝙕𝙀𝙉𝙍𝙊 𝙀𝙁𝙓⇜⃝𝄠⃝ │ *Place       :* ᴋᴇʀᴀʟᴀ │ *Gender   :*  ᴍᴀʟᴇ │ *Age          :* 1_ │ *Phone     :* wa.me/6282584996 │ *IG ID        :* fars33n │ *Status     :* _ ╰═════ꪶ ཻུ۪۪ꦽꦼ̷⸙ ━ ━ ━ ━ ꪶ ཻུ۪۪ꦽꦼ̷⸙}, {quoted: message.quoted || ''})
