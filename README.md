# AWS Solidus Demo Opsworks cookbook

This is a very basic Chef 13 cookbook that can be used to deploy Rails apps to AWS via OpsWorks. This cookbook accompanies this [blog post](https://nebulab.it/blog/solidus-deployment-amazon-aws-opsworks/) on Nebulab's technical blog. See the blog post for more details.

These are the steps used to generate this cookbook:

Install `chef`, then:

```bash
$ chef generate opsworks_cookbook
$ cd opsworks_cookbook

```

Edit `Berksfile` by adding:

```ruby
cookbook 'opsworks_ruby'
cookbook 'nodejs'
```

Add to `metadata.rb`:

```ruby
depends 'seven_zip', '~> 2.0'
```

And finally:

```bash
$ gem install berkshelf
$ berks install
$ berks package opsworks_cookbook.tar.gz

```
