# Spam Sarahah
Use this to spam sarahah users, because i got tired of all the sarahah statuses

##### NOTE: Sarahah allows users to report messages, so some users might not recieve messages, if you think that is the case, it is recommended that you log in your account in another tab(obviously a fake/dummy account). If that account is reported by the user too, create another ;)



## Steps
1. Open the sarahah page of the user you want to spam
2. Open `console` by pressing f12
3. Copy and paste the following script in console.
    
```    
var number = 50;
var message = 'hello sarahah';
var userId = $('#RecipientId').val();
verifTk = document.body.innerHTML.split("__RequestVerificationToken: $('")[1].split("').attr")[0];
for(i=0;i<number;i++){
    $.ajax({
        url: '/Messages/SendMessage',
        type: 'POST',
        cache: false,
        data: {
            __RequestVerificationToken: $(verifTk).attr('value'),
            userId: userId,
            text: message
        },
        success: function () {
           console.log("posted");
        },
        error: function () {
            console.log("error");
        }
    })
}
```

4. you will see `posted` in console, the number behind posted represents th number of times it has been posted.
5. There is no point 5, I am just adding this because a list with 5 points looks good. No, I don't have OCD.

#### Replace the top of the script with any number. the user gets the same message that number of times.
#### Replcae message with any message of your choice, but remember that the message should be placed between quotes.
