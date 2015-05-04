# basicrouter
<p>
This router is based on simonhamp/routes of which I forked months ago. There is nothing wrong about the original router. However, I decided to add another method to extract the controller and the controller method from the route() shown in the original class.
</p>

<h3> Example</h3>
<pre><code>
&lt;?php

include('router.php');

$routes = array(
       
        'controller/(:any)/(:any)/(:any)' => 'test/index/$1/$2/$3/',
        'register/' => 'MyController/myController_action'

        );
		
$url = 'dir/controller/method/param_one/param_two/param_threee';
$default_dir = ('dir/');
$request = trim(str_replace($default_dir, '', $url));		
		
Router::add($routes);
$action_request = Router::route($request);

print_r($action_request);

</code>
</pre>

