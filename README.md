# PHP Cheat Sheet
PHP Cheat Sheet with the most needed stuff..



## Prevent public user from accessing php files
```php
// method #1
// create in other document any element that will get sended via POST
if( !isset($_POST['access']) ){
   die('Direct access not permitted');
}

// method #2
// use .htaccess
// Deny from all
```




<br />
<br />


 _____________________________________________________
 _____________________________________________________


<br />
<br />

## Check if element exist
```php
if( !isset($_POST['access']) ){
   echo 'exist..';
}
```

<br />
<br />


 _____________________________________________________
 _____________________________________________________


<br />
<br />


# Email

## Send email
```php
<?PHP
$sender = 'info@fromwhocamethemail';
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

# Curl

## Get response of url
```php
$url = "https://www.google.com/recaptcha/api/siteverify?secret=6LeIxAcTAAAAAGG-vFI1TnRWxMZNFuojJ4WifJWe&response=".$captcha."&remoteip=".$_SERVER['REMOTE_ADDR'];
$curl = curl_init($url);

  curl_setopt($curl, CURLOPT_HTTPHEADER, array('Accept: application/json'));
  curl_setopt($curl, CURLOPT_RETURNTRANSFER, 1);
  $json = curl_exec($curl);
  //echo "request data: ".$json."\n\n";


    if(curl_errno($curl)){
        //echo 'Curl error: ' . curl_error($curl);
    }

```  



<br />
<br />


 _____________________________________________________
 _____________________________________________________


<br />
<br />

# JSON

## Parse JSON

```php
/*
{
  "success": true,
  "challenge_ts": "2020-07-23T23:39:14Z",
  "hostname": "testkey.google.com"
}
*/

//create object
$json = json_decode($data);
echo "success: ".$json->success;

// create array
$json = json_decode($data, true);
echo "success: ".$json["success"];
```

<br />
<br />


 _____________________________________________________
 _____________________________________________________


<br />
<br />
