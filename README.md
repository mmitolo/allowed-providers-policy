### Restrict GCP VM machine type

This policy uses the tfconfig/v2 import to restrict providers to those
in an allowed list.

It used to only use the providers collection of the tfconfig/v2 import, but
that did not process resources and data sources from allowed providers
when no provider block was included in the Terraform configuration. So, it now
also explicitly allows resources and data sources from allowed providers using
the resources collection of the tfconfig/v2 import.
