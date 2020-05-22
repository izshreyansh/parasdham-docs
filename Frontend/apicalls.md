# API Calls
In an SPA the most frequently used feature is calling the api to fetch / post data from the backend server. In order to concentrate api call logic into 1 file & provide support for DRY principles. We've abstracted out api calls in [Mixin](https://vuejs.org/v2/guide/mixins.html) file at `src\mixins\ApiMixin.js`.

In most of our view components you'll see call to backend in the following format:
```
this.callAPI({
    endpoint: `/tags/${this.id}`,
    type: 'get',
    successCallback: (response) => {
      this.tag = response.data;
    }
});
```
This snippet is delegating the call to API Mixin mentioned above. By providing callback functions to `successCallback` or `failureCallBack`. You can modify application behaviour on successful / failed api call.

If you simply want to print out confirmation received from api call, You can just set `sweetalert` property on the `callAPI` object to `true`. This will cause sweet alerts for api confirmation messages.