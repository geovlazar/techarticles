---
author: "Geo V L"
date: 2018-05-24
linktitle: Programmatic User creation and Welcome mail with customized contents from entities - Drupal 7
nomenu:
  main:
    parent: tutorials
next: /tutorials/Programmatic-User-creation-and-Welcome-mail-with-customized-contents-rom-entities
prev: /tutorials/programmatic-User-creation-and-Welcome-mail-with-customized-contents-rom-entities
title: Programmatic User creation and Welcome mail with customized contents from entities - Drupal 7
tags : [
    "Drupal",
    "development",
]
categories : ["CMS"]
weight: 10
image: img/writing.jpg
authorAvatar: hugo-logo.png
---



Consider a case that we need to add a drupal user when we create a content type and that specific drupal user has first name and last name and contact details from a node. Usual way to create a Drupal user is to use the method user_save as the following way. For sending message we can set default mail alert from "Configuration -> Account Settings -> Email Alerts Section " as explained below

```
    //set up the user fields
    $fields = array(
        'name' => $user_name,
        'mail' =>"mail@example.com",
        'pass' => "password",
        'status' => 1,
        'init' => ",
        'roles' => array(2 => TRUE, 3 => TRUE),
    );
    //print_r($fields);
    //the first parameter is left blank so a new user is created
    $account = user_save('', $fields);

    // If you want to send the welcome email, use the following code
    // Manually set the password so it appears in the e-mail.
    // $account->password = $fields['pass'];
    // Send the e-mail through the user module.
    drupal_mail(    
                    'user', 
                    'register_no_approval_required', 
                    "mail@example.com",
                     NULL, 
                     array('account' => $account
                    );

 ```