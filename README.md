# Traces

Traces is a micro CLI application that is able to get all contributions and their contributors in 
"developer-readable" JSON format for a specified repository.
 
 
## Installation
 
The authentication is a basic login/password for GitHub.
 
```bash
 $ composer require prestashop/traces
 
 $ ./vendor/bin/traces <repositoryOwner/repositoryName> <login> <password> --config="config.yml"
```
 
You can configure a list of excluded contributors, take a look to ```config.dist.yml``` file.
 
A file named ``contributors.js`` will be generated, you can manipulate it using any programming language.

### I prefer to export in XML/CSV/Whatever

This is not provided out of box right now. For CSV support take a look at [Json to CSV](https://konklone.io/json/) website, or to [csvkit](https://csvkit.readthedocs.io/en/latest/scripts/in2csv.html).

For XML, you may use [SimpleXMLElement](http://php.net/manual/fr/class.simplexmlelement.php). I'm open to contributions that allow to pass `--output=xml|csv|json` if the code remains simple.
