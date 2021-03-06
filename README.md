# Django-NumericFieldListFilter

Django-NumericFieldListFilter is a plugin for Django. It allows easy filtering of numeric fields (IntegerField, FloatField and DecimalField) inside the Django admin.

For each numeric field, two inputs will be added to the admin, representing a minimum and maximum value which you can filter on.

![Screenshot of NumericFieldListFilter](http://i.imgur.com/y6U9uCI.png)

### Installation

```sh
$ pip install django-numericfieldlistfilter
```

You'll need Django version 1.8 or greater.

### Usage
1. Add `djangonumericfieldlistfilter` to the installed apps:
    
    ```python
    INSTALLED_APPS = (
    ...
    'djangonumericfieldlistfilter',
    ...
    )
    ```
2. Use the `NumericModelAdmin` as the base class of your admin classes:
    ```python
    from djangonumericfieldlistfilter.options import NumericModelAdmin
    
    class TransactionAdmin(NumericModelAdmin):
        ...
    ```
3. Add your numeric field to the list_filter variable:

    ```python
    list_filter = (
        ...
        'price_paid'
        ...
    )
    ```

### Version
0.1

License
-------
MIT