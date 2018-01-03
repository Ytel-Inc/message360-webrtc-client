# WebRTC Client : 

## Installation Steps :

### 1. Clone repository:

 git clone https://github.com/Ytel-Inc/message360-webrtc-client

### 2. Navigate to ‘m360helper-v3/webrtc/’ and create .env file.
    .env file should contain ACCOUNT_SID and AUTH_TOKEN.
    Example: 
    
    .env
    ACCOUNT_SID=XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    AUTH_TOKEN=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

### 3. Navigate to ‘m360helper-v3/src/’ and create Configuration.php (if missing)

    

    Configuration.php

    <?php
/*
 * Message360
 *
 * This file was automatically generated for message360 by APIMATIC v2.0 ( https://apimatic.io ).
 */
 
namespace Message360Lib;
 
/**
 * All configuration including auth info and base URI for the API access
 * are configured in this class.
 */
class Configuration
{
    /**
     * The environment being used'
     * @var string
     */
    public static $environment = Environments::PRODUCTION;
 
    /**
     * The username to use with basic authentication
     * @var string
     */
    /**
     * @todo Replace the $basicAuthUserName with an appropriate value
     */
    public static $basicAuthUserName = 'TODO: Replace';
 
    /**
     * The password to use with basic authentication
     * @var string
     */
    /**
     * @todo Replace the $basicAuthPassword with an appropriate value
     */
    public static $basicAuthPassword = 'TODO: Replace';
    /**
     * Get the base uri for a given server in the current environment
     * @param  string $server Server name
     * @return string         Base URI
     */
    public static function getBaseUri($server = Servers::DEFAULT_)
    {
        return APIHelper::appendUrlWithTemplateParameters(
            static::$environmentsMap[static::$environment][$server],
            array(
            )
        );
    }
 
    /**
     * A map of all baseurls used in different environments and servers
     * @var array
     */
    private static $environmentsMap = array(
        Environments::PRODUCTION => array(
            Servers::DEFAULT_ => 'https://api.message360.com/api/v3',
        ),
    );
}


### 4. Navigate to ‘m360helper-v3’ and install composer
	
	Composer install

### 5. Navigate to root directory and adjust URLs for PHP files in ‘urlConfig.json’ file as per server configuration.




### 6. Install node dependencies : 

	npm install 

### 7 . Install bower dependencies

	bower install :

### 8 .Compile all javascript files 

           grunt default : 

### 9 Run  index.html  in browser 




