---
name: Rerequest a check suite
example: octokit.checks.rerequestSuite({ owner, repo, check_suite_id })
route: POST /repos/{owner}/{repo}/check-suites/{check_suite_id}/rerequest
scope: checks
type: API method
---

# Rerequest a check suite

Triggers GitHub to rerequest an existing check suite, without pushing new code to a repository. This endpoint will trigger the [`check_suite` webhook](https://developer.github.com/webhooks/event-payloads/#check_suite) event with the action `rerequested`. When a check suite is `rerequested`, its `status` is reset to `queued` and the `conclusion` is cleared.

To rerequest a check suite, your GitHub App must have the `checks:read` permission on a private repository or pull access to a public repository.

```js
octokit.checks.rerequestSuite({
  owner,
  repo,
  check_suite_id,
});
```

## Parameters

<table>
  <thead>
    <tr>
      <th>name</th>
      <th>required</th>
      <th>description</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>owner</td><td>yes</td><td>

</td></tr>
<tr><td>repo</td><td>yes</td><td>

</td></tr>
<tr><td>check_suite_id</td><td>yes</td><td>

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://developer.github.com/v3/checks/suites/#rerequest-a-check-suite).
