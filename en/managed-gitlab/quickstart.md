# Getting started with {{ mgl-name }}

To get started with the service:
1. [Create an instance](#instance-create).
1. [Set up a working environment](#configure-mgl).
1. [Get started with the repository](#start-work-with-git).

## Getting started {#before-you-begin}

{% list tabs %}

- Management console

  1. Go to the [management console]({{ link-console-main }}) and log in to {{ yandex-cloud }} or create an account if you do not have one yet.
  1. If you do not have a folder yet, create one:

     {% include [create-folder](../_includes/create-folder.md) %}

{% endlist %}

## Create an instance {#instance-create}

{% list tabs %}

- Management console

  {% include [instance-create-console](../_includes/managed-gitlab/instance-create-console.md) %}

{% endlist %}

## Set up a working environment {#configure-mgl}

In this section, you will learn how to prepare an instance {{ mgl-name }} to work.
1. [Configure the default security group](operations/connect.md#configuring-security-groups) for the cloud network to to enable all the relevant traffic.
1. Activate your instance {{ mgl-name }}:
   1. Follow the link sent to the administrator's email address when registering the instance.
   1. Change the administrator's password.
   1. Log in using the administrator's username and password.
1. [Create a group](https://docs.gitlab.com/ee/user/group/#create-a-group) that will host your project.
1. [Create a user](https://docs.gitlab.com/ee/user/profile/account/create_accounts.html) and [add them to the group](https://docs.gitlab.com/ee/user/project/members/#add-users-to-a-project) with the `Maintainer` or `Owner` role.
1. [Create and SSH key](https://docs.gitlab.com/ee/user/ssh.html) and [assign it to the user account](https://docs.gitlab.com/ee/ssh/#add-an-ssh-key-to-your-gitlab-account).
1. [Create an empty project](https://docs.gitlab.com/ee/user/project/) to host your repository.

## Get started with the repository {#start-work-with-git}

In this section, you will learn how to get started with a local copy of your repository under a created user. Perform these steps on the local computer:
1. [Install the Git client](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#install-git).
1. [Clone the repository](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#clone-a-repository) to the local machine.
1. Go to the directory with the repository:

   ```bash
   cd <project name>
   ```

1. Create a file named `README.md`:

   ```bash
   echo "This is my new project" > README.md
   ```

1. Index the `README.md` file:

   ```bash
   git add README.md
   ```

1. Apply the changes to the local repository using the command:

   ```bash
   git commit -m "Add README.md"
   ```

   For more information, see the [{{ GL }} documentation](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#add-and-commit-local-changes).

1. [Push the changes](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#send-changes-to-gitlabcom) to {{ mgl-name }}:

   ```bash
   git push origin main
   ```