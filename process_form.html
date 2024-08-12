<?php
// Check if the form is submitted
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    
    // Your Telegram Bot API token
    $botToken = "7141673102:AAFg0sRwQzwL7apL0zu6EsSlAmyIAUkaU2I";
    $groupChatID = -4242285242; // Your Telegram group chat ID
    
    // Define the upload directory
    $uploadDir = "uploads/";
    
    // Create the upload directory if it doesn't exist
    if (!file_exists($uploadDir)) {
        mkdir($uploadDir, 0777, true);
    }
    
    // Generate a unique submission number
    $submissionNumber = uniqid();
    
    // Process form data
    $name = $_POST["name"];
    $contactWhatsapp = $_POST["contact_whatsapp"];
    $contactTelegram = $_POST["contact_telegram"];
    $comment = $_POST["comment"];
    
    // Handle file upload
    $imageFileName = $name . "_" . basename($_FILES["image"]["name"]); // Rename image with person's name
    $targetFile = $uploadDir . $imageFileName;
    
    if (move_uploaded_file($_FILES["image"]["tmp_name"], $targetFile)) {
        // Save form data to a text file
        $fileData = "Submission Number: $submissionNumber\n";
        $fileData .= "Name: $name\n";
        $fileData .= "Contact Whatsapp: $contactWhatsapp\n";
        $fileData .= "Contact Telegram: $contactTelegram\n";
        $fileData .= "Comment: $comment\n";
        $fileData .= "Image Path: $targetFile\n\n";
        
        file_put_contents("data.txt", $fileData, FILE_APPEND | LOCK_EX);
        
        // Send the form data to Telegram group
        $telegramMessage = "New Form Submission:\n\n";
        $telegramMessage .= "Name: $name\n";
        $telegramMessage .= "Contact Whatsapp: $contactWhatsapp\n";
        $telegramMessage .= "Contact Telegram: $contactTelegram\n";
        $telegramMessage .= "Comment: $comment";
        
        // Send message to Telegram group
        $telegramUrl = "https://api.telegram.org/bot$botToken/sendMessage?chat_id=$groupChatID&text=" . urlencode($telegramMessage);
        file_get_contents($telegramUrl); // Send the message to the Telegram group
        
        // Display the form data on the website
        echo "<h2>Submitted Form:</h2>";
        echo "<p>Name: $name</p>";
        echo "<p>Contact Whatsapp: $contactWhatsapp</p>";
        echo "<p>Contact Telegram: $contactTelegram</p>";
        echo "<p>Comment: $comment</p>";
        
        echo "Form data saved successfully. Submission Number: $submissionNumber";
    } else {
        echo "Sorry, there was an error uploading your file.";
    }
} else {
    echo "Form submission error.";
}
?>
