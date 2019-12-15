# Obsess-Webhook
function postMessageToDiscord(message) {

  message = message || "Hello World!";
  
  var discordUrl = 'https://discordapp.com/api/webhooks/655703536524328979/zUv-RtJt73-TqltxAVuEzMnRkmoXtTib4R8OfRLNsJqDZRDFoQdFKJQhkgquhvb3z9u4';
  var payload = JSON.stringify({content: message});
  
  var params = {
    headers: {
      'Content-Type': 'application/x-www-form-urlencoded'
    },
    method: "POST",
    payload: payload,
    muteHttpExceptions: true
  };
  
  var response = UrlFetchApp.fetch(discordUrl, params);
  
  Logger.log(response.getContentText());

}
