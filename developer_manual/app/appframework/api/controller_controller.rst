Controller
==========


Baseclass to inherit your controllers from


.. php:namespace:: OCA\AppFramework\Controller
.. php:class:: Controller

  * **Abstract**


  .. php:attr:: $api
    
    * **Protected**
    
    None



  .. php:method:: __construct($api, $request)

    :param \\OCA\\AppFramework\\Core\\API $api: an api wrapper instance
    :param \\OCA\\AppFramework\\Http\\Request $request: an instance of the request



  .. php:method:: params($key, $default=null)

    :param string $key: the key which you want to access in the URL Parameter                    placeholder, $_POST or $_GET array.                    The priority how they're returned is the following:                    1. URL parameters                    2. POST parameters                    3. GET parameters
    :param mixed $default: If the key is not found, this value will be returned
    :returns mixed: the content of the array


    Lets you access post and get parameters by the index


  .. php:method:: getParams()

    :returns array: the array with all parameters


    Returns all params that were received, be it from the request(as GET or POST) or throuh the URL by the route


  .. php:method:: method()

    :returns string: the method of the request (POST, GET, etc)


    Returns the method of the request


  .. php:method:: getUploadedFile($key)

    :param string $key: the key that will be taken from the $_FILES array
    :returns array: the file in the $_FILES element


    Shortcut for accessing an uploaded file through the $_FILES array


  .. php:method:: env($key)

    :param string $key: the key that will be taken from the $_ENV array
    :returns array: the value in the $_ENV element


    Shortcut for getting env variables


  .. php:method:: session($key, $value=null)

    :param string $key: the key that will be taken from the $_SESSION array
    :param string $value: if given sets a new session variable
    :returns array: the value in the $_SESSION element


    Shortcut for getting and setting session variables


  .. php:method:: cookie($key)

    :param string $key: the key that will be taken from the $_COOKIE array
    :returns array: the value in the $_COOKIE element


    Shortcut for getting and setting cookie variables


  .. php:method:: render($templateName, $params=array(), $renderAs='user', $headers=array())

    :param string $templateName: the name of the template
    :param array $params: the template parameters in key => value structure
    :param string $renderAs: user renders a full page, blank only your template                         admin an entry in the admin settings
    :param array $headers: set additional headers
    :returns \\OCA\\AppFramework\\Http\\TemplateResponse: containing the page


    Shortcut for rendering a template


  .. php:method:: renderJSON($data=array(), $errorMsg=null)

    :param array $data: the PHP array that will be put into the JSON data indexempty by default
    :param string $errorMsg: If you want to return an error message, pass one
    :returns \\OCA\\AppFramework\\Http\\JSONResponse: containing the values


    Shortcut for rendering a JSON response


