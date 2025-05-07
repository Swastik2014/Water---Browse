# Water---Browse
This is a simple search engine which shows the search result using Bing.
It is an HTML Code, run it using browser.
Code:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>WaterBrowse</title>
    <script>
        function handleSearch(event) {
            event.preventDefault(); // Prevents default form submission
            let searchInput = document.getElementById("searchBox").value;
            
            // Check if the input is a valid URL
            if (searchInput.startsWith("http://") || searchInput.startsWith("https://")) {
                window.location.href = searchInput; // Redirects to the entered link
            } else {
                window.location.href = "https://www.bing.com/search?q=" + encodeURIComponent(searchInput);
            }
        }
    </script>
</head>
<body background="file:///C:/Users/bachh/OneDrive/Pictures/Screenshots/Screenshot%202025-05-07%20163151.png"
    style="background-size: cover; background-repeat: no-repeat; background-attachment: fixed;">
    
    <br><br>
    <center>
        <h1 style="color: white; font-size: 50px; font-family: Arial, Helvetica, sans-serif;">
            Water - Browse</h1>
        <p style="color: white; font-size: 20px; font-family: Arial, Helvetica, sans-serif;">
            Browse like Water</p>
        
        <br><br><br><br><br><br><br><br>

        <!-- Search Box -->
        <form onsubmit="handleSearch(event);">
            <input type="text" id="searchBox" name="q" placeholder="Search the web"
            style="width: 700px; height: 20px; font-size: 18px; padding: 10px;">
        </form>
    </center>
</body>
</html>
