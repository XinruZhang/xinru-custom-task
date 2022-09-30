# Wait Custom Task for Tekton

Install it by
```
ko apply -f config/controller
```

It implements `retries` and `timeout` as documented here https://tekton.dev/docs/pipelines/runs/#developer-guide-for-custom-controllers-supporting-timeout.

It marks the Run as `TimedOut` when the total run time reaches the limit, no matter wether the retries is exhausted or not.