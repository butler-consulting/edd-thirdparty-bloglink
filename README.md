EDD Third Party and Blog Link
=========

Allows you to add post meta data in Easy Digital Downloads to indicate a third party product, whether the download is a WordPress plugin and also a link for more information.

**This plugin requires [Easy Digital Downloads](http://wordpress.org/extend/plugins/easy-digital-downloads/ "Easy Digital Downloads"). It allows you to add post meta data in Easy Digital Downloads to indicate a third party product and also a link for more information. Also adds a checkbox to indicate if the download is available in the WordPress plugin repository. 

*Please Note: This plugin doesn't really do anything on it's own. This plugin is for advanced users and does nothing on the fron-end without writing your own custom code.*    

**Here is what it does do:**

* Adds a checkbox to the download configuration for you to indicate that a product is from a third party.
* Adds another checkbox to indicate that a product is available on the WordPress plugin repository.
* Adds a URL field for you to add an external link to a blog or website for product details or more information.
* Stores this data in the download product's post_meta data for you to access and use in your custom code.

**How to use in your code:**

```
if(get_post_meta( $post_id, 'edd_third_party', true )) {

    echo 'This item is from a third party.' ;

}
```

```
if(get_post_meta( $post_id, 'edd_wp_plugin', true )) {

    echo 'This item can be downloaded from WordPress.' ;

}
```

```
if(get_post_meta( $post_id, 'edd_bloglink_url', true )) {

    $bloglink = get_post_meta( $post_id, 'edd_bloglink_url', true );
    echo '<a href="' .$bloglink. '" target="_blank">Click for Details</a>';

}
```

Download it for free from the WordPress plugin repository here: http://wordpress.org/plugins/edd-thirdparty-bloglink/. Contributions, revisions, tweaks and critiques are always welcome!