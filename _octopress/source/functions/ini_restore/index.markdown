---
layout: page
title: "JavaScript ini_restore function"
comments: true
sharing: true
footer: true
sidebar: false
alias:
- /functions/view/ini_restore:599
- /functions/view/ini_restore
- /functions/view/599
- /functions/ini_restore:599
- /functions/599
---
<!-- Generated by Rakefile:build -->
A JavaScript equivalent of PHP's ini_restore

{% codeblock info/ini_restore.js lang:js https://raw.github.com/kvz/phpjs/master/functions/info/ini_restore.js raw on github %}
function ini_restore (varname) {
  // http://kevin.vanzonneveld.net
  // +   original by: Brett Zamir (http://brett-zamir.me)
  // *     example 1: ini_restore('date.timezone');
  // *     returns 1: 'America/Chicago'
  if (this.php_js && this.php_js.ini && this.php_js.ini[varname]) {
    this.php_js.ini[varname].local_value = this.php_js.ini[varname].global_value;
  }
}
{% endcodeblock %}

 - [view on github](https://github.com/kvz/phpjs/blob/master/functions/info/ini_restore.js)
 - [edit on github](https://github.com/kvz/phpjs/edit/master/functions/info/ini_restore.js)

### Example 1
This code
{% codeblock lang:js example %}
ini_restore('date.timezone');
{% endcodeblock %}

Should return
{% codeblock lang:js returns %}
'America/Chicago'
{% endcodeblock %}


### Other PHP functions in the info extension
{% render_partial _includes/custom/info.html %}
