# PHP Cheat Sheet
PHP Cheat Sheet with the most needed stuff..



# Email

## Send email
```php
<?PHP
$sender = 'info@fromwhocamethemeial';
$recipient = 'info@personwhorecivestheemail.com';

$subject = "php mail test";
$message = "php test message";
$headers = 'From:' . $sender;

if (mail($recipient, $subject, $message, $headers))
{
    echo "Message accepted";
}
else
{
    echo "Error: Message not accepted";
}
?>

```  



<br />
<br />


 _____________________________________________________
 _____________________________________________________


<br />
<br />
