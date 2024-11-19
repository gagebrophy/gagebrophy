chrome.webNavigation.onCompleted.addListener(function(details) {
  console.log('Visited: ', details.url);
  // Send this data to a server for monitoring
}, { url: [{ hostContains: 'schoolwebsite.com' }] });
chrome.tabs.query({active: true, currentWindow: true}, function(tabs) {
  console.log('Current tab URL:', tabs[0].url);
  // Send this data to a server for monitoring
});
