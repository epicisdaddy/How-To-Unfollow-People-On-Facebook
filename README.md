# How-To-Unfollow-People-On-Facebook
Facebook Unfollow all Script for firefox &amp; chrome
CODE -------

let intervalId = setInterval(function () {
let manageButtons = document.querySelectorAll('div[aria-label="Manage"]');
let manageButton = manageButtons[0];
if (manageButton) {

    setTimeout(() => {

        manageButton.click();
    }, 800);
    var unfollowButtons = null;
    let unfollowInterval = setInterval(function () {

        setTimeout(() => {

            unfollowButtons = document.querySelector('div[role="menuitem"]');
            if(unfollowButtons){
                unfollowButtons.click();
                window.scrollBy(0, 60);
            }
        }, 700);
        clearInterval(unfollowInterval);
    }, 700);
    setTimeout(() => {

        manageButton.remove();
        if(unfollowButtons){
            unfollowButtons.click();
        }
    }, 1000);
} else {
}
}, 700);
