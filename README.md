# FacebookInvitations
Script for quick-selecting all people in a to-invite list

1. Create a new event
2. Click on "Invite"
3. Select on the left a list of people you want to invite
4. Scroll down to the end of the list
5. Run the script
6. Enjoy how fast the counter goes up
7. Click on "Send Invititation"
8. Done, maybe give yourself some time-to-be for the time you saved :)

The script goes like this:

      function sleep(ms) {
        return new Promise(resolve => setTimeout(resolve, ms));
      }
      async function select() {
        var inputs = document.getElementsByClassName('_1pu2 _1pu4'); 
        while(inputs.length>0){
          //console.log(inputs.length);
          for(var i=0;i<inputs.length;i++) { 
            inputs[i].click(); 
            await sleep(1);   //Neccessary for the upwards counting effect
          }

          inputs = document.getElementsByClassName('_1pu2 _1pu4'); 
        }
      }
      select();
      
You enter it in the browsers javascript-console. You access it on Firefox via F12, on Chrom via Ctrl+Shift+J. Probably you have to declare yourself a web-developer by clicking ok if it is your first time doing such things.

Some tips:

- Facebook only allows 500 invitations per day
- The name of the Button ('_1pu2 _1pu4') may change in the future. It has already changed in the past. Please notify me here or on facebook if the script doesn't work anymore. It will probably because of this.
- There is a chrome extension for this but it had some bad reviews. No idea, it may do exactly the same. 
