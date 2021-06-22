# cfctl - CloudFlare Control  


A command line tool to do operations on cloudflare and avoid having to go into the web interface. 

[![Upload Python Package](https://github.com/jnvilo/cfctl/actions/workflows/python-publish.yml/badge.svg)](https://github.com/jnvilo/cfctl/actions/workflows/python-publish.yml)

## Configuration

cfctl connects to Cloudflare API using an api key. You can get the API key by logging to your cloudflare account and on the top right click "My Profile" in the dropdown and select the "API Tokens" tab. There you will see "Create API Key". 

Add these as environment variables to your .bashrc as :

    export CF_API_EMAIL=<your cloudflare account email>
    export CF_API_KEY=<Your API KEY>


## Usage

### adding a record 
    cfctl add_record -t 600 demo1.jnvilo.com A 192.168.100.1

### delete a record
     cfctl delete_record demo1.jnvilo.com 

### list all records
    cfctl list_records jnvilo.com 
    
### display entry
    cfctl inspect_fqdn demo1.jnvilo.com 
    
Test
---

    make test

You can also test with a specific version of Python:

    make PYTHON_VERSION=2.7.11 test
