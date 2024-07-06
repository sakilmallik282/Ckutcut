window.onload = function() {
    alert("Hey! Enjoying your visit? Install our app for more awesome features!");

    let views = 0;
    let popularity = 100;

    function increaseViews() {
        views++;
        document.getElementById('viewCount').textContent = views;
        console.log(`Current views: ${views}`);
    }

    function installAppPrompt() {
        const installConfirmed = confirm("Would you like to install our app for a better experience?");
        if (installConfirmed) {
            popularity += 10;
            document.getElementById('popularityCount').textContent = popularity;
            console.log(`Current popularity: ${popularity}`);
        }
    }

    document.getElementById('installAppButton').addEventListener('click', installAppPrompt);

    increaseViews();
};
