# Moonshine::Couchdb

## Introduction

Welcome to Moonshine::Couchdb, a [Moonshine](http://github.com/railsmachine/moonshine) plugin for installing and managing [couchdb](http://www.couchbase.com/products-and-services/couchbase-single-server)

Here's some quick links:

 * [Homepage](http://github.com/railsmachine/moonshine_couchdb)
 * [Issues](http://github.com/railsmachine/moonshine_couchdb/issues) 
 * [Wiki](http://github.com/railsmachine/moonshine_couchdb/wiki) 
 * [Mailing List](http://groups.google.com/group/railsmachine-moonshine)
 * Resources for using Couchdb:
   * [Couchdb Homepage](http://www.google.com/search?q=couchdb)

## Quick Start

Moonshine::Couchdb is installed as a Rails plugin:

    # Rails 2.x.x
    script/plugin install git://github.com/railsmachine/moonshine_couchdb.git
    # Rails 3.x.x
    script/rails plugin install git://github.com/railsmachine/moonshine_couchdb.git

Once it's installed, you can include it in your manifest:

    # app/manifests/application_manifest.rb
    class ApplicationManifest < Moonshine::Manifest:Rails

       # other recipes and configuration omitted

       # tell ApplicationManifest to use the couchdb recipe
       recipe :couchdb
    end

Ideally, things should work out of the box. If not, be sure to make the code detects missing configuration and fails with instructions. Also, include details about any required settings here.

## Configuration Options

Here's some other couchdb configuration options you may be interested in.

 * `:version`: a string representing the version to install

These are namespaced under `:couchdb`. They can be configured a few ways:

    # in global config/moonshine.yml
    :couchdb:
      :version: 1.1

    # in stage-specific moonshine.yml,
    # config/moonshine/staging.yml and config/moonshine/production.yml
    :couchdb:
      :version: 1.1

    # `configure` call in app/manifests/application_manifest.rb
    configure :couchdb => { :version => '1.1' }
