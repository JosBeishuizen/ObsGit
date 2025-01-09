# Git

Adres: https://github.com/JosBeishuizen/Logseq.git

command lin:
### …or create a new repository on the command line

echo "# Logseq" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/JosBeishuizen/Logseq.git
git push -u origin main

### …or push an existing repository from the command line

git remote add origin https://github.com/JosBeishuizen/Logseq.git
git branch -M main
git push -u origin main


Recovery codes
af7e6-1e397
3ef88-97d93
5a139-5dae6
060cf-93968
144b6-a24b6
b8e5f-a91cd
40631-ffcd8
b3092-d67a3
087e2-79e10
393bd-02837
4d85d-7f2c3
58f79-6425e
dfc0c-acd53
3bfd1-cca15
c5887-c97c3
1f1db-e1970

Authentication/Account security/Manage personal access tokens
Managing your personal access tokens
You can use a personal access token in place of a password when authenticating to GitHub in the command line or with the API.

In this article
About personal access tokens
Creating a fine-grained personal access token
Creating a personal access token (classic)
Deleting a personal access token
Using a personal access token on the command line
Further reading
Warning

Treat your access tokens like passwords. For more information, see Keeping your personal access tokens secure.

About personal access tokens
Personal access tokens are an alternative to using passwords for authentication to GitHub when using the GitHub API or the command line.

Personal access tokens are intended to access GitHub resources on behalf of yourself. To access resources on behalf of an organization, or for long-lived integrations, you should use a GitHub App. For more information, see About creating GitHub Apps.

A token has the same capabilities to access resources and perform actions on those resources that the owner of the token has, and is further limited by any scopes or permissions granted to the token. A token cannot grant additional access capabilities to a user. For example, a personal access token can be configured with an admin:org scope, but if the owner of the token is not an organization owner, the token will not give administrative access to the organization.

Types of personal access tokens
GitHub currently supports two types of personal access tokens: fine-grained personal access tokens and personal access tokens (classic). GitHub recommends that you use fine-grained personal access tokens instead of personal access tokens (classic) whenever possible.

Both fine-grained personal access tokens and personal access tokens (classic) are tied to the user who generated them and will become inactive if the user loses access to the resource.

Organization owners can set a policy to restrict the access of personal access tokens (classic) to their organization. For more information, see Setting a personal access token policy for your organization.

Fine-grained personal access tokens
Fine-grained personal access tokens have several security advantages over personal access tokens (classic):

Each token can only access resources owned by a single user or organization.
Each token can only access specific repositories.
Each token is granted specific permissions, which offer more control than the scopes granted to personal access tokens (classic).
Organization owners can require approval for any fine-grained personal access tokens that can access resources in the organization.
Personal access tokens (classic)
Personal access tokens (classic) are less secure. However, some features currently will only work with personal access tokens (classic):

Only personal access tokens (classic) have write access for public repositories that are not owned by you or an organization that you are not a member of.
Outside collaborators can only use personal access tokens (classic) to access organization repositories that they are a collaborator on.
A few REST API endpoints are only available with a personal access tokens (classic). To check whether an endpoint also supports fine-grained personal access tokens, see the documentation for that endpoint, or see Endpoints available for fine-grained personal access tokens.
If you choose to use a personal access token (classic), keep in mind that it will grant access to all repositories within the organizations that you have access to, as well as all personal repositories in your personal account.

As a security precaution, GitHub automatically removes personal access tokens that haven't been used in a year. To provide additional security, we highly recommend adding an expiration to your personal access tokens.

Keeping your personal access tokens secure
Personal access tokens are like passwords, and they share the same inherent security risks. Before creating a new personal access token, consider if there is a more secure method of authentication available to you:

To access GitHub from the command line, you can use GitHub CLI or Git Credential Manager instead of creating a personal access token.
When using a personal access token in a GitHub Actions workflow, consider whether you can use the built-in GITHUB_TOKEN instead. For more information, see Automatic token authentication.
If these options are not possible, and you must create a personal access token, consider using another CLI service to store your token securely.

When using a personal access token in a script, you can store your token as a secret and run your script through GitHub Actions. For more information, see Using secrets in GitHub Actions. You can also store your token as a Codespaces secret and run your script in Codespaces. For more information, see Managing your account-specific secrets for GitHub Codespaces.

For more information about best practices, see Keeping your API credentials secure.

Creating a fine-grained personal access token
Note

Fine-grained personal access token are currently in public preview and subject to change. To leave feedback, see the feedback discussion.

Verify your email address, if it hasn't been verified yet.

In the upper-right corner of any page on GitHub, click your profile photo, then click  Settings.

In the left sidebar, click  Developer settings.

In the left sidebar, under  Personal access tokens, click Fine-grained tokens.

Click Generate new token.

Under Token name, enter a name for the token.

Under Expiration, select an expiration for the token. Infinite lifetimes are allowed but may be blocked by a maximum lifetime policy set by your organization or enterprise owner. For more information, See Enforcing a maximum lifetime policy for personal access tokens.

Optionally, under Description, add a note to describe the purpose of the token.

Under Resource owner, select a resource owner. The token will only be able to access resources owned by the selected resource owner. Organizations that you are a member of will not appear unless the organization opted in to fine-grained personal access tokens. For more information, see Setting a personal access token policy for your organization.

Optionally, if the resource owner is an organization that requires approval for fine-grained personal access tokens, below the resource owner, in the box, enter a justification for the request.

Under Repository access, select which repositories you want the token to access. You should choose the minimal repository access that meets your needs. Tokens always include read-only access to all public repositories on GitHub.

If you selected Only select repositories in the previous step, under the Selected repositories dropdown, select the repositories that you want the token to access.

Under Permissions, select which permissions to grant the token. Depending on which resource owner and which repository access you specified, there are repository, organization, and account permissions. You should choose the minimal permissions necessary for your needs.

The REST API reference document for each endpoint states whether the endpoint works with fine-grained personal access tokens and states what permissions are required in order for the token to use the endpoint. Some endpoints may require multiple permissions, and some endpoints may require one of multiple permissions. For an overview of which REST API endpoints a fine-grained personal access token can access with each permission, see Permissions required for fine-grained personal access tokens.

Click Generate token.

If you selected an organization as the resource owner and the organization requires approval for fine-grained personal access tokens, then your token will be marked as pending until it is reviewed by an organization administrator. Your token will only be able to read public resources until it is approved. If you are an owner of the organization, your request is automatically approved. For more information, see Reviewing and revoking personal access tokens in your organization.

Creating a personal access token (classic)
Note

Organization owners can restrict the access of personal access token (classic) to their organization. If you try to use a personal access token (classic) to access resources in an organization that has disabled personal access token (classic) access, your request will fail with a 403 response. Instead, you must use a GitHub App, OAuth app, or fine-grained personal access token.

Warning

Your personal access token (classic) can access every repository that you can access. GitHub recommends that you use fine-grained personal access tokens instead, which you can restrict to specific repositories. Fine-grained personal access tokens also enable you to specify fine-grained permissions instead of broad scopes.

Verify your email address, if it hasn't been verified yet.

In the upper-right corner of any page on GitHub, click your profile photo, then click  Settings.

In the left sidebar, click  Developer settings.

In the left sidebar, under  Personal access tokens, click Tokens (classic).

Select Generate new token, then click Generate new token (classic).

In the "Note" field, give your token a descriptive name.

To give your token an expiration, select Expiration, then choose a default option or click Custom to enter a date.

Select the scopes you'd like to grant this token. To use your token to access repositories from the command line, select repo. A token with no assigned scopes can only access public information. For more information, see Scopes for OAuth apps.

Click Generate token.

Optionally, to copy the new token to your clipboard, click .

Screenshot of the "Personal access tokens" page. Next to a blurred-out token, an icon of two overlapping squares is outlined in orange.
To use your token to access resources owned by an organization that uses SAML single sign-on, authorize the token. For more information, see Authorizing a personal access token for use with SAML single sign-on in the GitHub Enterprise Cloud documentation.

