# Permissions

* Together with authentication and throttling, permissions determine whether a request should be granted or denied access.
* Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.

* Permissions are used to **grant** or **deny** access for different classes of users to different parts of the API.

## How permissions are determined

* Permissions in REST framework are always defined as a list of permission **classes**.

### When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

- The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.
- The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.
- The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.


## Object level permissions

Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

## Setting the permission policy

The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting. For example.

```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}

```

If not specified, this setting defaults to allowing unrestricted access:

```
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```


## API Reference

The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.

This permission is not strictly required, since you can achieve the same result by using an empty list or tuple for the permissions setting, but you may find it useful to specify this class because it makes the intention explicit.

* IsAuthenticated

    The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.

    This permission is suitable if you want your API to only be accessible to registered users.

* IsAdminUser

    The IsAdminUser permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.

    This permission is suitable if you want your API to only be accessible to a subset of trusted administrators.

* IsAuthenticatedOrReadOnly

    The IsAuthenticatedOrReadOnly will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS.

    This permission is suitable if you want to your API to allow read permissions to anonymous users, and only allow write permissions to authenticated users.



[For more information](https://www.django-rest-framework.org/api-guide/permissions/)