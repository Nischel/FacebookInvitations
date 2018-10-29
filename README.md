# FacebookInvitations
Script for quick-selecting all people in a to-invite list

1. Create a new event
2. Click on "Invite"
3. Select on the left a list of people you want to invite
4. Run the script
5. Enjoy how fast the counter goes up
6. Click on "Send Invititation"
7. Done, maybe give yourself some time-to-be for the time you saved :)

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
