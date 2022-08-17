# Fake Google Play Redemption Extension

This extension allows you to trick those pesky refund or tech support scammers (etc), into thinking that you are redeeming their giftcards.

This extension is avaliable for:
- **Chrome/Chromium Based Browsers (Brave, Edge, Opera, etc)**
- **Firefox**

If you don't have a payment method assigned to your account (this should be true, unless you want scammers to take your money), there won't be a google play balance thing on your screen usually. With this extension **it also adds your 'google play balance' on your screen**, it's also completely integrated with the extension. Whever you redeem something, the balance will be updated accordingly.

# How to enable your balance on the main payments screen
Press F12 or Ctrl-Shift-I, then go to 'Console', then type in (or copy and paste) the following:

```javascript

localStorage.setItem('balanceState', 'off')

```
Make sure to refresh afterwards.

# How to redeem a code
You need to include a certain number in the randomness you would put in the gift card input.
Here are some examples.

```
VALID CODE: DUEJ E01W DNRK SLRK - $10 (The 01 represents the amount)
```

```
INVALID CODE: D0EJ ED1W DNRK SLRK - Doesn't match with any amount.
```

**Here's a list of the only numbers you can use**
- 01: $10
- 02: $20
- 03: $30
- 04: $40
- 05: $50
- 06: $60
- 07: $70
- 08: $80
- 09: $90
- 10: $100
- 20: $200
- 30: $300
- 40: $400
- 50: $500

# How do I clear out my balance after bating? (optional)
Go back into your VM's console, then type in the following:
```javascript

localStorage.setItem('gpBalance', 0) // Clears Google Play Balance
localStorage.setItem('gcAmount', 0) // Clears Recent Gift Card Amount

```
# How to install
When you install this extension, in order to keep it hidden in case scammers want to see your extensions, the extension would be displayed as "Web Enhancer".
Make sure to keep the extension somewhere hidden from the scammers too. Or else they'll probably list all of the profanity they know, then hang up.

**Firefox:**
- Download the .xpi file
- Move the .xpi file somewhere secret and disguise it. I would also recommend renaming it to "web-enhancer"
- Go to the dropdown menu > Add-ons and themes
- Click on the cog icon and select "Install Add-on From File..."
- Then select the .xpi file wherever you stored it
- Click the "Add" button on the confirmation popup, then you're done!

**Chrome:**
- Download the .zip file
- Move it somewhere secret and disguise it. I would also recommend renaming it to "web-enhancer"
- Go to the dropdown menu > More tools > Extensions (or click on the extension puzzle icon, then go down to Manage extensions and click on that)
- Enable developer mode
- Drag and drop the zip file, you're done!

# Misc Information
Everything will be in USD within this extension, since even in the UK, it's easier to use VoIP services to call US numbers than UK numbers. If you wish to change the currency, you'll have to modify the code. If your currency is prone to high inflation (or has been in the past), then with basic javascript skills, you could change the gift card values too. If you're modifying the chrome version, you won't have any issues. But it's a lot more complicated for firefox, you'll need to look it up.
