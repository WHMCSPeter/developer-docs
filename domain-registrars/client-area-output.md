+++
prev = "/domain-registrars/module-logging/"
title = "Client Area Output"
weight = 100
+++

It is possible to output custom HTML in the Client Area when a client is viewing their domain name.

Using the `_ClientArea` function, you can return output, customised for the individual domain name being viewed.

Visit the [Module Parameters](https://developers.whmcs.com/domain-registrars/module-parameters/) page for information on 
the variables available in `$params`.

```
function registrarmodule_ClientArea($params)
{
    // Perform an API function call for any information
    // you wish to display here.

    $output = <<<HTML
<div class="alert alert-info">
    Your domain name is registered to {$params['fullname']}.
</div>
HTML;

    return $output;
}
```

