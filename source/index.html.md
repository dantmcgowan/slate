---
title: API Reference

language_tabs:
  - shell

toc_footers:
  - <a href="mailto:info@partner-path.com?subject=PartnerPath API key">Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# PartnerPath API Version 1

PartnerPath provides an Application Programming Interface for the various aspects of the Partner Portal application. Select from various *Controllers* to view documentation for classes and to learn how to use the API.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "http://#{client}|.#{environment}|.test.partnerpath.net/api/#{model.name.downcase.pluralize}"
  -H "Authorization: thepartnerpathtoken"
```

> Make sure to replace `thepartnerpathtoken` with your API key.

PartnerPath uses API keys to allow access to the API. You can register a new PartnerPath API key at our [developer portal](http://partner-path.com).

PartnerPath expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: thepartnerpathtoken`

<aside class="notice">
You must replace `thepartnerpathtoken` with your personal API key.
</aside>

# Companies

## Get All Companies

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  -s 'http://#{client}|.#{environment}|.test.partnerpath.net/api/companies' -i
```

> The above command returns JSON structured like this:

```json
[
{
  "companies": [
    {
      "name": "PayPal",
      "id": 150,
      "url": "http:\/\/paypal.com",
      "created_at": "2014-08-14T23:11:52.195Z",
      "updated_at": "2014-08-15T21:57:10.591Z",
      "is_partner": false,
      "parent_id": null,
      "company_type": null,
      "company_profile": {
        "overview": null,
        "solutions": null,
        "references": null,
        "quotes": null,
        "id": 2,
        "company_id": 150,
        "currency_id": 1,
        "active": true,
        "cogroup_id": 1,
        "business_unit_id": 1,
        "market_segment_ids": [
          "4",
          "5",
          "3",
          "1"
        ],
        "vertical_industry_ids": [
          "4",
          "1",
          "6"
        ],
        "engagement_level_ids": [
          "3",
          "1"
        ],
        "product_line_ids": [
          "3",
          "2",
          "4",
          "1"
        ],
        "registration_enabled": true,
        "log_in_enabled": true,
        "created_at": "2014-08-14T23:11:52.248Z",
        "updated_at": "2014-08-14T23:11:52.340Z",
        "display_company_profile": true,
        "cotype_ids": [
          "2",
          "4",
          "1",
          "3"
        ],
        "logo_file_name": null,
        "logo_content_type": null,
        "logo_file_size": null,
        "logo_updated_at": null,
        "account_manager_id": null,
        "custom": {
          "id": 1,
          "fields": {
            "certifications": "Global Accounts Administrator",
            "rank": "quarternary"
          },
          "customizable_id": 2,
          "customizable_type": "CompanyProfile",
          "created_at": "2014-08-14T23:11:52.293Z",
          "updated_at": "2014-08-14T23:11:52.293Z"
        }
      },
      "address": {
        "id": 1,
        "street": "2211 North First Street",
        "city": "San Jose",
        "state": "CA",
        "country": "US",
        "zip": "95131",
        "phone": "(402)935-2258",
        "fax": "(650)251-1101",
        "created_at": "2014-08-14T23:11:52.223Z",
        "updated_at": "2014-08-14T23:11:52.223Z",
        "addressable_type": "Company",
        "addressable_id": 150,
        "latitude": null,
        "longitude": null
      },
      "contacts": [
        {
          "id": 1,
          "contact_type_id": 1,
          "first_name": "Tavares",
          "last_name": "Reinger",
          "title": "Strategist",
          "email": "treinger@http:\/\/paypal.com",
          "phone": "1-614-921-6315",
          "mobile": null,
          "company_id": null,
          "created_at": "2014-08-14T23:11:52.264Z",
          "updated_at": "2014-08-14T23:11:52.264Z",
          "contactable_type": "Company",
          "contactable_id": 150
        }
      ],
      "geocoverage": {
        "id": 1,
        "coverable_id": 150,
        "coverable_type": "Company",
        "geography_ids": [

        ],
        "region_ids": [

        ],
        "country_codes": [
          "US"
        ],
        "created_at": "2014-08-14T23:11:52.211Z",
        "updated_at": "2014-08-14T23:11:52.325Z"
      }
    },
    {
      "name": "Pacocha Technologies",
      "id": 151,
      "url": "http:\/\/pacochatechnologies.com",
      "created_at": "2014-08-14T23:11:52.396Z",
      "updated_at": "2014-08-14T23:12:26.008Z",
      "is_partner": true,
      "parent_id": null,
      "company_type": null,
      "company_profile": {
        "overview": null,
        "solutions": null,
        "references": null,
        "quotes": null,
        "id": 3,
        "company_id": 151,
        "currency_id": null,
        "active": true,
        "cogroup_id": 2,
        "business_unit_id": 1,
        "market_segment_ids": [
          "1",
          "3",
          "5"
        ],
        "vertical_industry_ids": [
          "4",
          "1",
          "3",
          "5",
          "2"
        ],
        "engagement_level_ids": [
          "7",
          "1"
        ],
        "product_line_ids": [
          "3",
          "4",
          "2"
        ],
        "registration_enabled": true,
        "log_in_enabled": true,
        "created_at": "2014-08-14T23:11:52.423Z",
        "updated_at": "2014-08-14T23:11:52.465Z",
        "display_company_profile": true,
        "cotype_ids": [
          "2"
        ],
        "logo_file_name": null,
        "logo_content_type": null,
        "logo_file_size": null,
        "logo_updated_at": null,
        "account_manager_id": null
      },
      "address": {
        "id": 2,
        "street": "87081 Evalyn Alley",
        "city": "North Roycechester",
        "state": "CO",
        "country": "US",
        "zip": "89870-8987",
        "phone": "1-903-215-0461",
        "fax": null,
        "created_at": "2014-08-14T23:11:52.415Z",
        "updated_at": "2014-08-14T23:11:52.415Z",
        "addressable_type": "Company",
        "addressable_id": 151,
        "latitude": null,
        "longitude": null
      },
      "contacts": [
        {
          "id": 2,
          "contact_type_id": 1,
          "first_name": "Molly",
          "last_name": "Hills",
          "title": "Central Implementation Analyst",
          "email": "sheridan_wilderman@cremin.biz",
          "phone": "1-813-561-0183",
          "mobile": "1-817-812-5844",
          "company_id": null,
          "created_at": "2014-08-14T23:11:52.436Z",
          "updated_at": "2014-08-14T23:11:52.436Z",
          "contactable_type": "Company",
          "contactable_id": 151
        }
      ],
      "geocoverage": {
        "id": 2,
        "coverable_id": 151,
        "coverable_type": "Company",
        "geography_ids": [
          2
        ],
        "region_ids": [
          1,
          2,
          11
        ],
        "country_codes": [
          "WF",
          "JO",
          "BQ",
          "BE",
          "GS",
          "BH",
          "ZA",
          "AO",
          "ST",
          "VU",
          "BG",
          "SZ",
          "SC",
          "FO",
          "KZ",
          "KP",
          "IN",
          "SK",
          "GG",
          "GP",
          "BB",
          "KE",
          "TF",
          "HM"
        ],
        "created_at": "2014-08-14T23:11:52.405Z",
        "updated_at": "2014-08-14T23:11:52.458Z"
      }
    }
  ],
  "message": "OK"
}
]
```

This endpoint retrieves all companies.

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/companies`

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

## Get a Specific Company

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  'http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/152' -i
```

> The above command returns JSON structured like this:

```json
{
  "company": {
    "name": "Adaptive Support",
    "id": 152,
    "url": "http:\/\/www.adaptivesupport.com",
    "created_at": "2014-08-14T23:11:52.497Z",
    "updated_at": "2015-01-13T16:59:16.424Z",
    "is_partner": true,
    "parent_id": null,
    "company_type": "partner",
    "partner_application_id": null,
    "company_profile": {
      "overview": "Steady performer, low turnover. Many holidays.",
      "solutions": "Competitive. Delicate but unassuming.",
      "references": "Larry. Moe. Curly.",
      "quotes": "Best Company. Ever.",
      "id": 4,
      "company_id": 152,
      "currency_id": 1,
      "active": true,
      "cogroup_id": 4,
      "business_unit_id": 2,
      "market_segment_ids": [
        "2",
        "4"
      ],
      "vertical_industry_ids": [
        "3"
      ],
      "engagement_level_ids": [
        "1",
        "2",
        "3"
      ],
      "product_line_ids": [
        "2",
        "3"
      ],
      "registration_enabled": true,
      "log_in_enabled": true,
      "created_at": "2014-08-14T23:11:52.523Z",
      "updated_at": "2015-01-13T16:59:16.407Z",
      "display_company_profile": true,
      "cotype_ids": [
        "1"
      ],
      "logo_file_name": null,
      "logo_content_type": null,
      "logo_file_size": null,
      "logo_updated_at": null,
      "account_manager_id": null,
      "external_id": "",
      "custom": {
        "id": 5,
        "fields": {
          "custom_paypal_cobranded_url": "www.paypal.com",
          "custom_paypal_merchant_i_d": "38special",
          "custom_paypal_implementation_url": "www.paypal.com",
          "custom_paypal_short_description": "we are the best",
          "custom_paypal_referral_i_d": "58long",
          "custom_paypal_product_expertise": [
            "",
            "",
            "14"
          ],
          "custom_paypal_bn_code": {
            "bn_code_1": "PPDec9_test_123_2",
            "bn_code_2": "PPDec9_test",
            "bn_code_3": "PPDec9_test_123_k",
            "bn_code_4": "PPDec9_test_as_11",
            "bn_code_5": "PPDec9_test_1111_12",
            "bn_code_6": "PPDec9_test_123444_12"
          },
          "custom_paypal_relationship_manager_name": "Steven Hauschka"
        },
        "customizable_id": 4,
        "customizable_type": "CompanyProfile",
        "created_at": "2014-09-29T17:19:27.669Z",
        "updated_at": "2015-01-13T16:59:16.392Z"
      },
      "contracts": [
        {
          "id": 23,
          "contractable_id": 4,
          "contractable_type": "CompanyProfile",
          "fee": null,
          "start_date": "2012-12-09",
          "end_date": "2016-12-09",
          "auto_start_date": null,
          "auto_end_date": null,
          "created_at": "2014-12-09T19:18:31.058Z",
          "updated_at": "2014-12-09T19:18:31.058Z",
          "signatory_name": null,
          "signatory_email": null,
          "agreements": [
            {
              "id": 29,
              "name": "NA2016 Specialty",
              "external_agreement_id": null,
              "created_at": "2015-01-13T01:23:29.145Z",
              "updated_at": "2015-01-13T01:23:29.145Z",
              "content_file_name": null,
              "content_content_type": null,
              "content_file_size": null,
              "content_updated_at": null,
              "is_custom": false,
              "agreement_type": "Standard",
              "title": "Special NA2016 2016"
            },
            {
              "id": 30,
              "name": "NA2017 Standard",
              "external_agreement_id": null,
              "created_at": "2015-01-13T01:23:29.302Z",
              "updated_at": "2015-01-13T01:23:29.302Z",
              "content_file_name": null,
              "content_content_type": null,
              "content_file_size": null,
              "content_updated_at": null,
              "is_custom": false,
              "agreement_type": "Standard",
              "title": "Standard NA2017 2017"
            }
          ]
        }
      ]
    },
    "address": {
      "id": 3,
      "street": "23220 Peggie Turnpike",
      "city": "Alexiston",
      "state": "IA",
      "country": "US",
      "zip": "19565-1106",
      "phone": "709-941-3982",
      "fax": "709-941-3900",
      "created_at": "2014-08-14T23:11:52.515Z",
      "updated_at": "2015-01-13T16:59:16.356Z",
      "addressable_type": "Company",
      "addressable_id": 152,
      "latitude": null,
      "longitude": null
    },
    "contacts": [
      {
        "id": 3,
        "contact_type_id": 1,
        "first_name": "Ashtyn",
        "last_name": "Mosciski",
        "title": "Chief Accounts Strategist",
        "email": "joan.herzog@paucekkoepp.info",
        "phone": "1-516-830-3150",
        "mobile": "1-207-698-9789",
        "company_id": null,
        "created_at": "2014-08-14T23:11:52.535Z",
        "updated_at": "2014-08-14T23:11:52.535Z",
        "contactable_type": "Company",
        "contactable_id": 152
      }
    ],
    "geocoverage": {
      "id": 3,
      "coverable_id": 152,
      "coverable_type": "Company",
      "geography_ids": [
        "6"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2014-08-14T23:11:52.506Z",
      "updated_at": "2015-01-13T16:59:16.338Z"
    }
  },
  "message": "OK"
}
```

This endpoint retrieves a specific company.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Company to retrieve

## Create a Company

```shell
  curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X POST --data @thumper.json 'http://demopath.test:3000/api/companies'
```
> thumper.json:

```
{
  "company": {
    "name": "Thumper",
    "url": "http:\/\/www.thumper.com",
    "is_partner": true,
    "active": true,
    "company_type": "partner",
    "company_profile": {
      "cogroup": "Gold",
      "business_unit": "Automation",
      "engagement_levels": "OEM",
      "product_lines": "Malbec",
      "market_segments": "Service Offering",
      "vertical_industries": "Finance",
      "cotypes": "System Integrator"
    },
    "address": {
      "street": "Test Street",
      "city": "Test City",
      "state": "WA",
      "country": "US",
      "zip": "98001",
      "phone": "206-999-9999"
    },
    "domains": [
      {
        "name": "thumper.com",
        "active": true
      }
    ],
    "contacts": [
      {
        "contact_type_id": 1,
        "first_name": "Jane",
        "last_name": "Doe",
        "title": "King of the Jungle",
        "email": "jd@thumper.com",
        "phone": "206-999-9999"
      }
    ],
    "geocoverage": {
      "geography_ids": [
        2
      ]
    }
  }
}
```
> The above command returns JSON structured like this:

```json
{
  "company": {
    "name": "Thumper",
    "id": 6868,
    "url": "http:\/\/www.thumper.com",
    "is_partner": true,
    "active": true,
    "company_type": "partner",
    "parent_id": null,
    "partner_application_id": null,
    "inactive_date": null,
    "deleted": false,
    "deleted_at": null,
    "deleted_by_user_id": null,
    "created_at": "2016-07-27T17:24:56.410Z",
    "updated_at": "2016-07-27T17:24:56.410Z",
    "company_profile": {
      "overview": null,
      "solutions": null,
      "references": null,
      "quotes": null,
      "id": 496,
      "company_id": 6868,
      "currency_id": null,
      "active": true,
      "registration_enabled": true,
      "log_in_enabled": true,
      "created_at": "2016-07-27T17:24:56.533Z",
      "updated_at": "2016-07-27T17:24:56.533Z",
      "display_company_profile": true,
      "logo_file_name": null,
      "logo_content_type": null,
      "logo_file_size": null,
      "logo_updated_at": null,
      "account_manager_id": null,
      "external_id": "",
      "office_manager_id": null,
      "vendor_visible": true,
      "sfdc_id": null,
      "directory_enabled_at": null,
      "contracts": [
        
      ],
      "cogroup": "Gold",
      "business_unit": null,
      "engagement_levels": "OEM",
      "product_lines": "Malbec",
      "market_segments": "Service Offering",
      "vertical_industries": "Finance",
      "cotypes": "System Integrator"
    },
    "address": {
      "id": 3044,
      "street": "Test Street",
      "city": "Test City",
      "state": "WA",
      "country": "US",
      "zip": "98001",
      "phone": "206-999-9999",
      "fax": null,
      "created_at": "2016-07-27T17:24:56.495Z",
      "updated_at": "2016-07-27T17:24:56.495Z",
      "addressable_type": "Company",
      "addressable_id": 6868,
      "latitude": null,
      "longitude": null
    },
    "domains": [
      {
        "id": 7003,
        "company_id": 6868,
        "name": "thumper.com",
        "active": true,
        "created_at": "2016-07-27T17:24:56.418Z",
        "updated_at": "2016-07-27T17:24:56.418Z"
      }
    ],
    "contacts": [
      {
        "id": 3044,
        "contact_type_id": 1,
        "first_name": "Jane",
        "last_name": "Doe",
        "title": "King of the Jungle",
        "email": "jd@thumper.com",
        "phone": "206-999-9999",
        "mobile": null,
        "company_id": null,
        "created_at": "2016-07-27T17:24:56.563Z",
        "updated_at": "2016-07-27T17:24:56.563Z",
        "contactable_type": "Company",
        "contactable_id": 6868,
        "sfdc_id": null
      }
    ],
    "geocoverage": {
      "id": 596,
      "coverable_id": 6868,
      "coverable_type": "Company",
      "created_at": "2016-07-27T17:24:56.460Z",
      "updated_at": "2016-07-27T17:24:56.460Z",
      "geography_ids": [
        2
      ],
      "region_ids": [
        
      ],
      "country_codes": [
        
      ]
    }
  },
  "message": "OK"
}
```

This endpoint creates a specific Company.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`POST http://#{client}|.#{environment}|.test.partnerpath.net/api/companies`


## Update a Specific Company

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"company": {"url": "http://adaptivesupport.com", "company_profile": {"cogroup": "Platinum"}}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/152'
```

> The above command returns JSON structured like this:

```json
{
  "company": {
    "name": "Adaptive Support",
    "id": 152,
    "url": "http:\/\/adaptivesupport.com",
    "created_at": "2014-08-14T23:11:52.497Z",
    "updated_at": "2015-02-25T01:06:49.094Z",
    "is_partner": true,
    "parent_id": null,
    "company_type": "partner",
    "partner_application_id": null,
    "company_profile": {
      "overview": "Steady performer, low turnover. Many holidays.",
      "solutions": "Competitive. Delicate but unassuming.",
      "references": "Larry. Moe. Curly.",
      "quotes": "Best Company. Ever.",
      "id": 4,
      "company_id": 152,
      "currency_id": 1,
      "active": true,
      "registration_enabled": true,
      "log_in_enabled": true,
      "created_at": "2014-08-14T23:11:52.523Z",
      "updated_at": "2015-02-25T01:06:49.140Z",
      "display_company_profile": true,
      "logo_file_name": "mariners.jpg",
      "logo_content_type": "image\/jpeg",
      "logo_file_size": 9065,
      "logo_updated_at": "2015-01-28T19:49:13.163Z",
      "account_manager_id": null,
      "external_id": "",
      "custom": {
        "id": 5,
        "fields": {
          "custom_paypal_cobranded_url": "www.paypal.com",
          "custom_paypal_merchant_i_d": "38special",
          "custom_paypal_implementation_url": "www.paypal.com",
          "custom_paypal_short_description": "we are the best",
          "custom_paypal_referral_i_d": "58long",
          "custom_paypal_product_expertise": [
            "",
            ""
          ],
          "custom_paypal_bn_code": {
            "bn_code_1": "PPDec9_test_123_2",
            "bn_code_2": "PPDec9_test",
            "bn_code_3": "PPDec9_test_123_k",
            "bn_code_4": "PPDec9_test_as_11",
            "bn_code_5": "PPDec9_test_1111_12",
            "bn_code_6": "PPDec9_test_123444_12",
            "bn_code_7": "SSample_BN_EC_US Program",
            "bn_code_8": "SSample2_BN2_EC_US"
          },
          "custom_paypal_relationship_manager_name": "Steven Hauschka",
          "custom_paypal_referral_link": "867-5309"
        },
        "customizable_id": 4,
        "customizable_type": "CompanyProfile",
        "created_at": "2014-09-29T17:19:27.669Z",
        "updated_at": "2015-02-25T00:26:51.553Z"
      },
      "contracts": [
        {
          "id": 23,
          "contractable_id": 4,
          "contractable_type": "CompanyProfile",
          "fee": null,
          "start_date": "2012-12-09",
          "end_date": "2016-12-09",
          "auto_start_date": null,
          "auto_end_date": null,
          "created_at": "2014-12-09T19:18:31.058Z",
          "updated_at": "2014-12-09T19:18:31.058Z",
          "signatory_name": null,
          "signatory_email": null,
          "agreements": [

          ]
        }
      ],
      "cogroup": "Platinum",
      "business_unit": "Implementation",
      "engagement_levels": "Managed - PM, Managed - POD, Self-serve",
      "product_lines": "Adaptive Payments, Braintree v.zero",
      "market_segments": "Hosting Services, Software Offering",
      "vertical_industries": "Entertainment",
      "cotypes": "Financial Institution"
    },
    "address": {
      "id": 3,
      "street": "23220 Peggie Turnpike",
      "city": "Alexiston",
      "state": "IA",
      "country": "US",
      "zip": "19565-1106",
      "phone": "709-941-3982",
      "fax": "709-941-3901",
      "created_at": "2014-08-14T23:11:52.515Z",
      "updated_at": "2015-02-20T00:43:23.091Z",
      "addressable_type": "Company",
      "addressable_id": 152,
      "latitude": null,
      "longitude": null
    },
    "contacts": [
      {
        "id": 3,
        "contact_type_id": 1,
        "first_name": "Ashtyn",
        "last_name": "Mosciski",
        "title": "Chief Accounts Strategist",
        "email": "joan.herzog@paucekkoepp.info",
        "phone": "1-516-830-3150",
        "mobile": "1-207-698-9789",
        "company_id": null,
        "created_at": "2014-08-14T23:11:52.535Z",
        "updated_at": "2014-08-14T23:11:52.535Z",
        "contactable_type": "Company",
        "contactable_id": 152
      }
    ],
    "geocoverage": {
      "id": 3,
      "coverable_id": 152,
      "coverable_type": "Company",
      "geography_ids": [
        "6"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2014-08-14T23:11:52.506Z",
      "updated_at": "2015-02-25T01:06:49.105Z"
    }
  },
  "message": "OK"
}
```

This endpoint updates a specific company.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Company to update

## Add Contract(s) to a Specific Company

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"company": {"contracts":[ {"name": "NA2016 Specialty", "title": "Special NA2016 2016", "type": "Standard", "start_date" : "2016-11-17", "end_date" : "2017-11-17"}, {"name": "NA2017 Standard", "title": "Standard NA2017 2017", "type": "Standard", "start_date" : "2017-11-17", "end_date" : "2018-11-17"}]}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/add_contracts/152'
```

> The above command returns JSON structured like this:

```json
{
  "company": {
    "name": "Adaptive Support",
    "id": 152,
    "url": "http:\/\/www.adaptivesupport.com",
    "created_at": "2014-08-14T23:11:52.497Z",
    "updated_at": "2015-01-09T19:29:51.343Z",
    "is_partner": true,
    "parent_id": null,
    "company_type": "partner",
    "partner_application_id": null,
    "company_profile": {
      "overview": "",
      "solutions": "",
      "references": "",
      "quotes": "",
      "id": 4,
      "company_id": 152,
      "currency_id": 1,
      "active": true,
      "cogroup_id": 4,
      "business_unit_id": 2,
      "market_segment_ids": [
        "2",
        "4"
      ],
      "vertical_industry_ids": [
        "3"
      ],
      "engagement_level_ids": [
        "1",
        "2",
        "3"
      ],
      "product_line_ids": [
        "2",
        "3"
      ],
      "registration_enabled": true,
      "log_in_enabled": true,
      "created_at": "2014-08-14T23:11:52.523Z",
      "updated_at": "2015-01-13T01:23:29.323Z",
      "display_company_profile": true,
      "cotype_ids": [
        "1"
      ],
      "logo_file_name": null,
      "logo_content_type": null,
      "logo_file_size": null,
      "logo_updated_at": null,
      "account_manager_id": null,
      "external_id": "",
      "custom": {
        "id": 5,
        "fields": {
          "custom_paypal_cobranded_url": "www.paypal.com",
          "custom_paypal_merchant_i_d": "",
          "custom_paypal_implementation_url": "www.paypal.com",
          "custom_paypal_short_description": "we are the best",
          "custom_paypal_referral_i_d": "",
          "custom_paypal_product_expertise": [
            "",
            ""
          ],
          "custom_paypal_bn_code": {
            "bn_code_1": "PPDec9_test_123_2",
            "bn_code_2": "PPDec9_test",
            "bn_code_3": "PPDec9_test_123_k",
            "bn_code_4": "PPDec9_test_as_11",
            "bn_code_5": "PPDec9_test_1111_12",
            "bn_code_6": "PPDec9_test_123444_12"
          }
        },
        "customizable_id": 4,
        "customizable_type": "CompanyProfile",
        "created_at": "2014-09-29T17:19:27.669Z",
        "updated_at": "2014-12-09T18:54:46.890Z"
      },
      "contracts": [
        {
          "id": 23,
          "contractable_id": 4,
          "contractable_type": "CompanyProfile",
          "fee": null,
          "start_date": "2012-12-09",
          "end_date": "2016-12-09",
          "auto_start_date": null,
          "auto_end_date": null,
          "created_at": "2014-12-09T19:18:31.058Z",
          "updated_at": "2014-12-09T19:18:31.058Z",
          "signatory_name": null,
          "signatory_email": null,
          "agreements": [
            {
              "id": 29,
              "name": "NA2016 Specialty",
              "external_agreement_id": null,
              "created_at": "2015-01-13T01:23:29.145Z",
              "updated_at": "2015-01-13T01:23:29.145Z",
              "content_file_name": null,
              "content_content_type": null,
              "content_file_size": null,
              "content_updated_at": null,
              "is_custom": false,
              "agreement_type": "Standard",
              "title": "Special NA2016 2016"
            },
            {
              "id": 30,
              "name": "NA2017 Standard",
              "external_agreement_id": null,
              "created_at": "2015-01-13T01:23:29.302Z",
              "updated_at": "2015-01-13T01:23:29.302Z",
              "content_file_name": null,
              "content_content_type": null,
              "content_file_size": null,
              "content_updated_at": null,
              "is_custom": false,
              "agreement_type": "Standard",
              "title": "Standard NA2017 2017"
            }
          ]
        }
      ]
    },
    "address": {
      "id": 3,
      "street": "23220 Peggie Turnpike",
      "city": "Alexiston",
      "state": "IA",
      "country": "US",
      "zip": "19565-1106",
      "phone": "709-941-3982",
      "fax": "",
      "created_at": "2014-08-14T23:11:52.515Z",
      "updated_at": "2014-12-05T21:37:40.197Z",
      "addressable_type": "Company",
      "addressable_id": 152,
      "latitude": null,
      "longitude": null
    },
    "contacts": [
      {
        "id": 3,
        "contact_type_id": 1,
        "first_name": "Ashtyn",
        "last_name": "Mosciski",
        "title": "Chief Accounts Strategist",
        "email": "joan.herzog@paucekkoepp.info",
        "phone": "1-516-830-3150",
        "mobile": "1-207-698-9789",
        "company_id": null,
        "created_at": "2014-08-14T23:11:52.535Z",
        "updated_at": "2014-08-14T23:11:52.535Z",
        "contactable_type": "Company",
        "contactable_id": 152
      }
    ],
    "geocoverage": {
      "id": 3,
      "coverable_id": 152,
      "coverable_type": "Company",
      "geography_ids": [
        "6"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2014-08-14T23:11:52.506Z",
      "updated_at": "2014-12-05T21:37:40.180Z"
    }
  },
  "message": "OK"
}
```

This endpoint adds Contract(s) to a specific company.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/add_contracts/<ID>`
`PUT http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/add_contracts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Company

## Remove bn_code(s) from a Specific Company

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"company": {"bn_codes":[ {"bn_code": "SSample2_BN2_EC_US"}]}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/remove_bn_codes/152'
```

> The above command returns JSON structured like this:

```json
{
  "company": {
    "name": "Adaptive Support",
    "id": 152,
    "url": "http:\/\/www.adaptivesupport.com",
    "created_at": "2014-08-14T23:11:52.497Z",
    "updated_at": "2014-12-03T02:51:20.529Z",
    "is_partner": true,
    "parent_id": null,
    "company_type": "partner",
    "external_id": "",
    "partner_application_id": null,
    "company_profile": {
      "overview": "",
      "solutions": "",
      "references": "",
      "quotes": "",
      "id": 4,
      "company_id": 152,
      "currency_id": null,
      "active": true,
      "cogroup_id": 4,
      "business_unit_id": 2,
      "market_segment_ids": [
        "2",
        "4"
      ],
      "vertical_industry_ids": [
        "3"
      ],
      "engagement_level_ids": [
        "1",
        "2",
        "3"
      ],
      "product_line_ids": [
        "2",
        "3"
      ],
      "registration_enabled": true,
      "log_in_enabled": true,
      "created_at": "2014-08-14T23:11:52.523Z",
      "updated_at": "2014-12-03T02:54:52.470Z",
      "display_company_profile": true,
      "cotype_ids": [
        "1"
      ],
      "logo_file_name": null,
      "logo_content_type": null,
      "logo_file_size": null,
      "logo_updated_at": null,
      "account_manager_id": null,
      "custom": {
        "id": 5,
        "fields": {
          "custom_paypal_cobranded_url": "www.paypal.com",
          "custom_paypal_merchant_i_d": "",
          "custom_paypal_implementation_url": "www.paypal.com",
          "custom_paypal_short_description": "we are the best",
          "custom_paypal_referral_i_d": "",
          "custom_paypal_product_expertise": [
            "",
            ""
          ],
          "custom_paypal_bn_code": {
            "bn_code_1": "SSample_BN_EC_US Program"
          }
        },
        "customizable_id": 4,
        "customizable_type": "CompanyProfile",
        "created_at": "2014-09-29T17:19:27.669Z",
        "updated_at": "2014-12-03T02:54:52.750Z"
      },
      "contracts": [
        {
          "id": 19,
          "contractable_id": 4,
          "contractable_type": "CompanyProfile",
          "fee": null,
          "start_date": "2012-12-03",
          "end_date": "2016-12-03",
          "auto_start_date": null,
          "auto_end_date": null,
          "created_at": "2014-12-03T02:13:11.394Z",
          "updated_at": "2014-12-03T02:13:11.394Z",
          "signatory_name": null,
          "signatory_email": null,
          "agreements": [
            {
              "id": 27,
              "name": "NA2016 Specialty",
              "external_agreement_id": null,
              "created_at": "2014-12-03T01:56:50.731Z",
              "updated_at": "2014-12-03T01:56:50.731Z",
              "content_file_name": null,
              "content_content_type": null,
              "content_file_size": null,
              "content_updated_at": null,
              "is_custom": false,
              "agreement_type": "Standard"
            },
            {
              "id": 28,
              "name": "NA2017 Standard",
              "external_agreement_id": null,
              "created_at": "2014-12-03T01:56:50.886Z",
              "updated_at": "2014-12-03T01:56:50.886Z",
              "content_file_name": null,
              "content_content_type": null,
              "content_file_size": null,
              "content_updated_at": null,
              "is_custom": false,
              "agreement_type": "Standard"
            }
          ]
        }
      ]
    },
    "address": {
      "id": 3,
      "street": "23220 Peggie Turnpike",
      "city": "Alexiston",
      "state": "IA",
      "country": "US",
      "zip": "19565-1106",
      "phone": "1-709-941-3986",
      "fax": "",
      "created_at": "2014-08-14T23:11:52.515Z",
      "updated_at": "2014-09-29T17:20:01.162Z",
      "addressable_type": "Company",
      "addressable_id": 152,
      "latitude": null,
      "longitude": null
    },
    "contacts": [
      {
        "id": 3,
        "contact_type_id": 1,
        "first_name": "Ashtyn",
        "last_name": "Mosciski",
        "title": "Chief Accounts Strategist",
        "email": "joan.herzog@paucekkoepp.info",
        "phone": "1-516-830-3150",
        "mobile": "1-207-698-9789",
        "company_id": null,
        "created_at": "2014-08-14T23:11:52.535Z",
        "updated_at": "2014-08-14T23:11:52.535Z",
        "contactable_type": "Company",
        "contactable_id": 152
      }
    ],
    "geocoverage": {
      "id": 3,
      "coverable_id": 152,
      "coverable_type": "Company",
      "geography_ids": [
        "6"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2014-08-14T23:11:52.506Z",
      "updated_at": "2014-11-25T02:42:54.109Z"
    }
  },
  "message": "OK"
}
```

This endpoint removes bn_code(s) from a specific company.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/remove_bn_codes/<ID>`
`PUT http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/remove_bn_codes/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Company

## Add bn_code(s) to a Specific Company

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"company": {"bn_codes":[ {"bn_code": "SSample_BN_EC_US Program"}, {"bn_code": "SSample2_BN2_EC_US"}]}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/add_bn_codes/152'
```

> The above command returns JSON structured like this:

```json
{
  "company": {
    "name": "Adaptive Support",
    "id": 152,
    "url": "http:\/\/www.adaptivesupport.com",
    "created_at": "2014-08-14T23:11:52.497Z",
    "updated_at": "2014-12-03T02:46:51.474Z",
    "is_partner": true,
    "parent_id": null,
    "company_type": "partner",
    "external_id": "",
    "partner_application_id": null,
    "company_profile": {
      "overview": "",
      "solutions": "",
      "references": "",
      "quotes": "",
      "id": 4,
      "company_id": 152,
      "currency_id": null,
      "active": true,
      "cogroup_id": 4,
      "business_unit_id": 2,
      "market_segment_ids": [
        "2",
        "4"
      ],
      "vertical_industry_ids": [
        "3"
      ],
      "engagement_level_ids": [
        "1",
        "2",
        "3"
      ],
      "product_line_ids": [
        "2",
        "3"
      ],
      "registration_enabled": true,
      "log_in_enabled": true,
      "created_at": "2014-08-14T23:11:52.523Z",
      "updated_at": "2014-12-03T02:51:19.944Z",
      "display_company_profile": true,
      "cotype_ids": [
        "1"
      ],
      "logo_file_name": null,
      "logo_content_type": null,
      "logo_file_size": null,
      "logo_updated_at": null,
      "account_manager_id": null,
      "custom": {
        "id": 5,
        "fields": {
          "custom_paypal_cobranded_url": "www.paypal.com",
          "custom_paypal_merchant_i_d": "",
          "custom_paypal_implementation_url": "www.paypal.com",
          "custom_paypal_short_description": "we are the best",
          "custom_paypal_referral_i_d": "",
          "custom_paypal_product_expertise": [
            "",
            ""
          ],
          "custom_paypal_bn_code": {
            "bn_code_1": "SSample_BN_EC_US Program",
            "bn_code_2": "SSample2_BN2_EC_US"
          }
        },
        "customizable_id": 4,
        "customizable_type": "CompanyProfile",
        "created_at": "2014-09-29T17:19:27.669Z",
        "updated_at": "2014-12-03T02:51:20.200Z"
      },
      "contracts": [
        {
          "id": 19,
          "contractable_id": 4,
          "contractable_type": "CompanyProfile",
          "fee": null,
          "start_date": "2012-12-03",
          "end_date": "2016-12-03",
          "auto_start_date": null,
          "auto_end_date": null,
          "created_at": "2014-12-03T02:13:11.394Z",
          "updated_at": "2014-12-03T02:13:11.394Z",
          "signatory_name": null,
          "signatory_email": null,
          "agreements": [
            {
              "id": 27,
              "name": "NA2016 Specialty",
              "external_agreement_id": null,
              "created_at": "2014-12-03T01:56:50.731Z",
              "updated_at": "2014-12-03T01:56:50.731Z",
              "content_file_name": null,
              "content_content_type": null,
              "content_file_size": null,
              "content_updated_at": null,
              "is_custom": false,
              "agreement_type": "Standard"
            },
            {
              "id": 28,
              "name": "NA2017 Standard",
              "external_agreement_id": null,
              "created_at": "2014-12-03T01:56:50.886Z",
              "updated_at": "2014-12-03T01:56:50.886Z",
              "content_file_name": null,
              "content_content_type": null,
              "content_file_size": null,
              "content_updated_at": null,
              "is_custom": false,
              "agreement_type": "Standard"
            }
          ]
        }
      ]
    },
    "address": {
      "id": 3,
      "street": "23220 Peggie Turnpike",
      "city": "Alexiston",
      "state": "IA",
      "country": "US",
      "zip": "19565-1106",
      "phone": "1-709-941-3986",
      "fax": "",
      "created_at": "2014-08-14T23:11:52.515Z",
      "updated_at": "2014-09-29T17:20:01.162Z",
      "addressable_type": "Company",
      "addressable_id": 152,
      "latitude": null,
      "longitude": null
    },
    "contacts": [
      {
        "id": 3,
        "contact_type_id": 1,
        "first_name": "Ashtyn",
        "last_name": "Mosciski",
        "title": "Chief Accounts Strategist",
        "email": "joan.herzog@paucekkoepp.info",
        "phone": "1-516-830-3150",
        "mobile": "1-207-698-9789",
        "company_id": null,
        "created_at": "2014-08-14T23:11:52.535Z",
        "updated_at": "2014-08-14T23:11:52.535Z",
        "contactable_type": "Company",
        "contactable_id": 152
      }
    ],
    "geocoverage": {
      "id": 3,
      "coverable_id": 152,
      "coverable_type": "Company",
      "geography_ids": [
        "6"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2014-08-14T23:11:52.506Z",
      "updated_at": "2014-11-25T02:42:54.109Z"
    }
  },
  "message": "OK"
}
```

This endpoint adds bn_code(s) to a specific company.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/add_bn_codes/<ID>`
`PUT http://#{client}|.#{environment}|.test.partnerpath.net/api/companies/add_bn_codes/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Company

# Contacts

## Get All Contacts

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  -s 'http://#{client}|.#{environment}|.test.partnerpath.net/api/contacts' -i
```

> The above command returns JSON structured like this:

```json
[
{
  "contacts": [
    {
      "id": 1,
      "contact_type_id": 1,
      "first_name": "Tavares",
      "last_name": "Reinger",
      "title": "Strategist",
      "email": "treinger@http:\/\/paypal.com",
      "phone": "1-614-921-6315",
      "mobile": null,
      "company_id": null,
      "created_at": "2014-08-14T23:11:52.264Z",
      "updated_at": "2014-08-14T23:11:52.264Z",
      "contactable_type": "Company",
      "contactable_id": 150
    },
    {
      "id": 2,
      "contact_type_id": 1,
      "first_name": "Molly",
      "last_name": "Hills",
      "title": "Central Implementation Analyst",
      "email": "sheridan_wilderman@cremin.biz",
      "phone": "1-813-561-0183",
      "mobile": "1-817-812-5844",
      "company_id": null,
      "created_at": "2014-08-14T23:11:52.436Z",
      "updated_at": "2014-08-14T23:11:52.436Z",
      "contactable_type": "Company",
      "contactable_id": 151
    },
    {
      "id": 20,
      "contact_type_id": 1,
      "first_name": "Pauline",
      "last_name": "Smitham",
      "title": "Human Research Administrator",
      "email": "margie@schuppe.info",
      "phone": "1-809-893-9445",
      "mobile": "1-800-325-3535",
      "company_id": null,
      "created_at": "2014-08-14T23:11:54.396Z",
      "updated_at": "2014-08-18T21:26:33.075Z",
      "contactable_type": "Company",
      "contactable_id": 169
    }
  ],
  "message": "OK"
}
]
```

This endpoint retrieves all companies.

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/contacts`

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

## Get a Specific Contact

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  'http://#{client}|.#{environment}|.test.partnerpath.net/api/contacts/20' -i
```

> The above command returns JSON structured like this:

```json
{
  "contact": {
    "id": 20,
    "contact_type_id": 1,
    "first_name": "Pauline",
    "last_name": "Smitham",
    "title": "Human Research Administrator",
    "email": "margie@schuppe.info",
    "phone": "1-809-893-9445",
    "mobile": "1-800-325-3535",
    "company_id": null,
    "created_at": "2014-08-14T23:11:54.396Z",
    "updated_at": "2014-08-18T21:26:33.075Z",
    "contactable_type": "Company",
    "contactable_id": 169
  },
  "message": "OK"
}
```

This endpoint retrieves a specific contact.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/contacts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Contact to retrieve

## Update a Specific Contact

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"contact": {"first_name": "Julius"}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/contacts/20'
```

> The above command returns JSON structured like this:

```json
{
  "contact": {
    "id": 20,
    "contact_type_id": 1,
    "first_name": "Julius",
    "last_name": "Smitham",
    "title": "Human Research Administrator",
    "email": "margie@schuppe.info",
    "phone": "1-809-893-9445",
    "mobile": "1-800-325-3535",
    "company_id": null,
    "created_at": "2014-08-14T23:11:54.396Z",
    "updated_at": "2014-08-18T23:23:00.274Z",
    "contactable_type": "Company",
    "contactable_id": 169
  },
  "message": "OK"
}
```

This endpoint updates a specific contact.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/contacts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Contact to update

# Deals

## Get All Deals

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  -s 'http://#{client}|.#{environment}|.test.partnerpath.net/api/deals' -i
```

> The above command returns JSON structured like this:

```json
[
{
  "deals": [
    {
      "id": 36,
      "workflow_status": "Submitted",
      "approval_status": "pending_level_one",
      "external_lead_id": "0064000000dcUcHAAU",
      "company_id": 281,
      "user_id": 1880,
      "contact_id": null,
      "prospect_company_name": "DB Systel GmbH",
      "prospect_company_url": "www.dbsystel.de",
      "lead_name": "DB Systel Goes TBM",
      "lead_type_id": 3,
      "vertical_industry_ids": null,
      "product_line_ids": null,
      "info_solutions": null,
      "info_generated": "Performed performance review and strategic discussion",
      "info_new_lead": null,
      "lead_source_id": 1,
      "prior_sales_rep": null,
      "currency_id": 4,
      "revenue_license": 0,
      "revenue_service": 0,
      "revenue_support": 0,
      "sales_stage_id": 1,
      "close_probability": null,
      "estimated_close_date": "2015-09-30",
      "partner_contact_comments": "",
      "admin_new_lead": null,
      "actual_close_date": null,
      "referral_fee_status_id": null,
      "referral_amount_paid": null,
      "referral_paid_date": null,
      "created_at": "2015-02-20T20:27:16.670Z",
      "updated_at": "2015-02-20T20:27:33.482Z",
      "from_api": false,
      "reassignment_flag": false,
      "address": {
        "id": 88,
        "street": "Jocrgen-Ponto-Platz 1",
        "city": "Frankfurt am Main",
        "state": "HE",
        "country": "DE",
        "zip": "60329",
        "phone": "+49 69 26550000",
        "fax": "",
        "created_at": "2015-02-20T20:27:16.677Z",
        "updated_at": "2015-02-20T20:27:33.437Z",
        "addressable_type": "Deal",
        "addressable_id": 36,
        "latitude": 50.10967,
        "longitude": 8.66893
      },
      "contact": {
        "id": 92,
        "contact_type_id": 1,
        "first_name": "Thomas",
        "last_name": "Dr. Ditzer",
        "title": "Head of Business Development",
        "email": "TDitzer@deutschebahn.com",
        "phone": "+49 69 26550000",
        "mobile": "",
        "company_id": null,
        "created_at": "2015-02-20T20:27:16.728Z",
        "updated_at": "2015-02-20T20:27:16.728Z",
        "contactable_type": "Deal",
        "contactable_id": 36
      },
      "custom": {
        "id": 70,
        "fields": {
          "custom_apptio_vertical_industry": "Transportation",
          "custom_apptio_prior_sales_rep": "false",
          "custom_apptio_strategic_initiatives": "Cost Reduction, Private\/Public Cloud, Shared Services",
          "custom_apptio_primary_competitor": "HP",
          "response_percentage": null
        },
        "customizable_id": 36,
        "customizable_type": "Deal",
        "created_at": "2015-02-20T20:27:16.606Z",
        "updated_at": "2015-02-20T20:27:16.766Z"
      },
      "user": {
        "email": "frank.bastian@isg-one.com",
        "first_name": "Frank",
        "last_name": "Bastian"
      },
      "company": {
        "name": "ISG (Information Services Group)",
        "id": 281,
        "url": "www.isg-one.com",
        "created_at": "2015-01-17T08:05:04.153Z",
        "updated_at": "2015-03-02T22:05:18.184Z",
        "is_partner": true,
        "parent_id": null,
        "company_type": "partner",
        "partner_application_id": null,
        "address": {
          "street": "Two Stamford Plaza 281 Tresser Boulevard",
          "city": "Stamford",
          "state": "CT",
          "country": "US",
          "zip": "06901",
          "phone": "(203) 5173100"
        }
      }
    },
    {
      "id": 37,
      "workflow_status": "Submitted",
      "approval_status": "pending_level_one",
      "external_lead_id": null,
      "company_id": 281,
      "user_id": 1880,
      "contact_id": null,
      "prospect_company_name": "Next New Company",
      "prospect_company_url": "http:\/\/nnc.com",
      "lead_name": "Tanforan",
      "lead_type_id": 1,
      "info_solutions": "Risk ",
      "info_generated": "Partner Conference",
      "info_new_lead": true,
      "lead_source_id": 2,
      "prior_sales_rep": "No",
      "currency_id": 1,
      "revenue_license": 900000,
      "revenue_service": 22000,
      "revenue_support": 40000,
      "sales_stage_id": 3,
      "close_probability": "88",
      "estimated_close_date": "2015-05-30",
      "partner_contact_comments": "Strong lead",
      "admin_new_lead": false,
      "actual_close_date": null,
      "referral_fee_status_id": 5,
      "referral_amount_paid": "2200",
      "referral_paid_date": null,
      "created_at": "2015-03-02T22:05:17.290Z",
      "updated_at": "2015-03-02T22:05:17.647Z",
      "from_api": true,
      "reassignment_flag": false,
      "custom": {
        "id": 85,
        "fields": {
          "custom_apptio_primary_competitor": "HP",
          "custom_apptio_strategic_initiatives": "App Rat",
          "custom_apptio_prior_sales_rep": "false",
          "custom_apptio_vertical_industry": "Transportation"
        },
        "customizable_id": 37,
        "customizable_type": "Deal",
        "created_at": "2015-03-02T22:05:17.461Z",
        "updated_at": "2015-03-02T22:05:17.461Z"
      },
      "user": {
        "email": "frank.bastian@isg-one.com",
        "first_name": "Frank",
        "last_name": "Bastian"
      },
      "company": {
        "name": "ISG (Information Services Group)",
        "id": 281,
        "url": "www.isg-one.com",
        "created_at": "2015-01-17T08:05:04.153Z",
        "updated_at": "2015-03-02T22:05:18.184Z",
        "is_partner": true,
        "parent_id": null,
        "company_type": "partner",
        "partner_application_id": null,
        "address": {
          "street": "Two Stamford Plaza 281 Tresser Boulevard",
          "city": "Stamford",
          "state": "CT",
          "country": "US",
          "zip": "06901",
          "phone": "(203) 5173100"
        }
      },
      "product_lines": "Cost Transparency, Business Insights",
      "vertical_industries": "Healthcare Providers, Utilities"
    }
  ],
  "message": "OK"
}
]
```

This endpoint retrieves all Deals.

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/deals`

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

## Get a Specific Deal

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  'http://#{client}|.#{environment}|.test.partnerpath.net/api/deals/30' -i
```

> The above command returns JSON structured like this:

```json
{
  "deal": {
    "id": 30,
    "workflow_status": "Submitted",
    "approval_status": "pending_level_one",
    "external_lead_id": "0064000000dB0wtAAC",
    "company_id": 277,
    "user_id": 1573,
    "contact_id": null,
    "prospect_company_name": "Test For Partner Portal 2",
    "prospect_company_url": "www.djklfads.com",
    "lead_name": "Test for SFDC Pushback",
    "lead_type_id": 4,
    "info_solutions": null,
    "info_generated": "kljbnlknjlkjn",
    "info_new_lead": null,
    "lead_source_id": 1,
    "prior_sales_rep": null,
    "currency_id": 7,
    "revenue_license": 0,
    "revenue_service": 0,
    "revenue_support": 0,
    "sales_stage_id": 1,
    "close_probability": null,
    "estimated_close_date": "2015-03-31",
    "partner_contact_comments": "",
    "admin_new_lead": null,
    "actual_close_date": null,
    "referral_fee_status_id": null,
    "referral_amount_paid": null,
    "referral_paid_date": null,
    "created_at": "2015-02-06T19:26:24.590Z",
    "updated_at": "2015-03-02T19:15:01.982Z",
    "from_api": true,
    "reassignment_flag": false,
    "address": {
      "id": 78,
      "street": "None O Yo Biznesses Drive",
      "city": "Nope",
      "state": "BAL",
      "country": "AF",
      "zip": "",
      "phone": "555-555-5555",
      "fax": "",
      "created_at": "2015-02-06T19:26:24.598Z",
      "updated_at": "2015-03-02T16:24:00.797Z",
      "addressable_type": "Deal",
      "addressable_id": 30,
      "latitude": null,
      "longitude": null
    },
    "contact": {
      "id": 82,
      "contact_type_id": 1,
      "first_name": "test",
      "last_name": "tres",
      "title": "Assistant to the Regional Manager",
      "email": "test@test.com",
      "phone": "555-555-5555",
      "mobile": "",
      "company_id": null,
      "created_at": "2015-02-06T19:26:24.650Z",
      "updated_at": "2015-03-02T16:01:14.968Z",
      "contactable_type": "Deal",
      "contactable_id": 30
    },
    "custom": {
      "id": 52,
      "fields": {
        "custom_apptio_vertical_industry": "Chemicals",
        "custom_apptio_strategic_initiatives": "DC Consolidation",
        "custom_apptio_primary_competitor": "VMWare (DigitalFuel)",
        "response_percentage": null
      },
      "customizable_id": 30,
      "customizable_type": "Deal",
      "created_at": "2015-02-06T19:26:24.414Z",
      "updated_at": "2015-02-06T19:26:24.695Z"
    },
    "user": {
      "email": "apcuser@apptio.com",
      "first_name": "APC",
      "last_name": "User"
    },
    "company": {
      "name": "Test Partner - APC",
      "id": 277,
      "url": "www.testpartnerapc.com",
      "created_at": "2015-01-14T19:20:51.398Z",
      "updated_at": "2015-03-02T19:15:02.341Z",
      "is_partner": true,
      "parent_id": null,
      "company_type": "partner",
      "partner_application_id": null,
      "address": {
        "street": "15200 NE 16th Place",
        "city": "Bellevue",
        "state": "WA",
        "country": "US",
        "zip": "98004",
        "phone": "4259741326"
      }
    },
    "product_lines": "Cost Transparency, Business Insights",
    "vertical_industries": "Healthcare Providers, Utilities"
  },
  "message": "OK"
}
```

This endpoint retrieves a specific Deal.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/deals/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Deal to retrieve

## Create a Deal

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH \
--data '{"deal":{
"workflow_status":"new",
"company_id":"281",
"custom_apptio_vertical_industry": "Food and Beverage Processing",
"custom_apptio_prior_sales_rep": "false",
"custom_apptio_strategic_initiatives": "App Rat",
"custom_apptio_primary_competitor": "HP",
"response_percentage": "77",
"user_id":1880,"prospect_company_name":"Hotdoggers",
"prospect_company_url":"http://triumph.com","lead_name":"Quantum",
"lead_type_id":1,"vertical_industries":  "Industrial Electronics and Electrical Equipment",
"product_lines" : "Cost Transparency, Business Insights",
"info_solutions":"Risk ","info_generated":"Partner Conference",
"info_new_lead":true,"lead_source_id":"2",
"prior_sales_rep":"No","currency_id":1,
"revenue_license":"500000","revenue_service":"500000","revenue_support":"500000",
"sales_stage_id":3,"close_probability":"88",
"estimated_close_date":"2015-05-30","partner_contact_comments":"Strong lead",
"admin_new_lead":false,"referral_fee_status_id":5,
"referral_amount_paid":"10000",
"address":{"street":"1428 Biscayne way",
"city":"Miami","state":"FL","country":"US","zip":"36751",
"phone":"315-555-7531","addressable_type":"Deal","latitude":25.7886172,"longitude":-80.1891029},
"contact":{"contact_type_id":1,"first_name":"Amerigo","last_name":"Vespucci",
"title":"Assistant to the Regional Manager","email":"avespucci@hotdoggers.com",
"phone":"315-555-7536"}}}' \
'http://#{client}|.#{environment}|.test.partnerpath.net/api/deals'
```

> The above command returns JSON structured like this:

```json
{
  "deal": {
    "id": 41,
    "workflow_status": "submitted",
    "approval_status": "pending_level_one",
    "external_lead_id": null,
    "company_id": 281,
    "user_id": 1880,
    "contact_id": null,
    "prospect_company_name": "Hotdoggers",
    "prospect_company_url": "http:\/\/triumph.com",
    "lead_name": "Quantum",
    "lead_type_id": 1,
    "info_solutions": "Risk ",
    "info_generated": "Partner Conference",
    "info_new_lead": true,
    "lead_source_id": 2,
    "prior_sales_rep": "No",
    "currency_id": 1,
    "revenue_license": 500000,
    "revenue_service": 500000,
    "revenue_support": 500000,
    "sales_stage_id": 3,
    "close_probability": "88",
    "estimated_close_date": "2015-05-30",
    "partner_contact_comments": "Strong lead",
    "admin_new_lead": false,
    "actual_close_date": null,
    "referral_fee_status_id": 5,
    "referral_amount_paid": "10000",
    "referral_paid_date": null,
    "created_at": "2015-03-05T19:48:50.943Z",
    "updated_at": "2015-03-05T19:48:50.943Z",
    "from_api": true,
    "reassignment_flag": false,
    "address": {
      "id": 89,
      "street": "1428 Biscayne way",
      "city": "Miami",
      "state": "FL",
      "country": "US",
      "zip": "36751",
      "phone": "315-555-7531",
      "fax": null,
      "created_at": "2015-03-05T19:48:50.952Z",
      "updated_at": "2015-03-05T19:48:50.952Z",
      "addressable_type": "Deal",
      "addressable_id": 41,
      "latitude": null,
      "longitude": null
    },
    "contact": {
      "id": 93,
      "contact_type_id": 1,
      "first_name": "Amerigo",
      "last_name": "Vespucci",
      "title": "Assistant to the Regional Manager",
      "email": "avespucci@hotdoggers.com",
      "phone": "315-555-7536",
      "mobile": null,
      "company_id": null,
      "created_at": "2015-03-05T19:48:51.008Z",
      "updated_at": "2015-03-05T19:48:51.008Z",
      "contactable_type": "Deal",
      "contactable_id": 41
    },
    "custom": {
      "id": 95,
      "fields": {
        "custom_apptio_primary_competitor": "HP",
        "custom_apptio_strategic_initiatives": "App Rat",
        "custom_apptio_prior_sales_rep": "false",
        "custom_apptio_vertical_industry": "Food and Beverage Processing"
      },
      "customizable_id": 41,
      "customizable_type": "Deal",
      "created_at": "2015-03-05T19:48:51.084Z",
      "updated_at": "2015-03-05T19:48:51.084Z"
    },
    "user": {
      "email": "frank.bastian@isg-one.com",
      "first_name": "Frank",
      "last_name": "Bastian"
    },
    "company": {
      "name": "ISG (Information Services Group)",
      "id": 281,
      "url": "www.isg-one.com",
      "created_at": "2015-01-17T08:05:04.153Z",
      "updated_at": "2015-03-05T19:48:51.130Z",
      "is_partner": true,
      "parent_id": null,
      "company_type": "partner",
      "partner_application_id": null,
      "address": {
        "street": "Two Stamford Plaza 281 Tresser Boulevard",
        "city": "Stamford",
        "state": "CT",
        "country": "US",
        "zip": "06901",
        "phone": "(203) 5173100"
      }
    },
    "product_lines": "Cost Transparency, Business Insights",
    "vertical_industries": "Industrial Electronics and Electrical Equipment"
  },
  "message": "OK"
}
```

This endpoint creates a specific Deal.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`POST http://#{client}|.#{environment}|.test.partnerpath.net/api/deals`


## Update a Specific Deal

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"deal": {"contact": {"title" : "Assistant to the Regional Manager"},"address": {"street" : "None O Yo Biznesses Drive"}, "product_lines" : "Cost Transparency, Business Insights", "vertical_industries" :"Healthcare Providers, Utilities"}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/deals/28'
```

> The above command returns JSON structured like this:

```json
{
  "deal": {
    "id": 28,
    "workflow_status": "submitted",
    "approval_status": "pending_level_one",
    "external_lead_id": "0064000000d9XdIAAU",
    "company_id": 267,
    "user_id": 1591,
    "contact_id": null,
    "prospect_company_name": "BC Hydro",
    "prospect_company_url": "www.bchydro.com",
    "lead_name": "IT Planning",
    "lead_type_id": 5,
    "info_solutions": null,
    "info_generated": "Avantage relationship",
    "info_new_lead": null,
    "lead_source_id": 1,
    "prior_sales_rep": null,
    "currency_id": 3,
    "revenue_license": 50000,
    "revenue_service": 100000,
    "revenue_support": 0,
    "sales_stage_id": 1,
    "close_probability": null,
    "estimated_close_date": "2015-04-30",
    "partner_contact_comments": "",
    "admin_new_lead": null,
    "actual_close_date": null,
    "referral_fee_status_id": null,
    "referral_amount_paid": null,
    "referral_paid_date": null,
    "created_at": "2015-01-30T17:37:53.704Z",
    "updated_at": "2015-03-05T19:54:14.575Z",
    "from_api": true,
    "reassignment_flag": false,
    "address": {
      "id": 76,
      "street": "None O Yo Biznesses Drive",
      "city": "Vancouver",
      "state": "BC",
      "country": "CA",
      "zip": "V6B 5R3",
      "phone": "604 224 9376 ",
      "fax": "",
      "created_at": "2015-01-30T17:37:53.711Z",
      "updated_at": "2015-03-05T19:54:14.422Z",
      "addressable_type": "Deal",
      "addressable_id": 28,
      "latitude": 49.2817781,
      "longitude": -123.1127576
    },
    "contact": {
      "id": 80,
      "contact_type_id": 1,
      "first_name": "Adam",
      "last_name": "Frecnh",
      "title": "Assistant to the Regional Manager",
      "email": "afrench@bchydro.com",
      "phone": "604 224 9376 ",
      "mobile": "",
      "company_id": null,
      "created_at": "2015-01-30T17:37:53.760Z",
      "updated_at": "2015-03-05T19:54:14.499Z",
      "contactable_type": "Deal",
      "contactable_id": 28
    },
    "custom": {
      "id": 44,
      "fields": {
        "custom_apptio_vertical_industry": "Energy",
        "custom_apptio_prior_sales_rep": "false",
        "custom_apptio_strategic_initiatives": "Outsourcing",
        "custom_apptio_primary_competitor": "VMWare (DigitalFuel)",
        "response_percentage": null
      },
      "customizable_id": 28,
      "customizable_type": "Deal",
      "created_at": "2015-01-30T17:37:53.504Z",
      "updated_at": "2015-01-30T17:37:53.795Z"
    },
    "user": {
      "email": "trevor.kray@avantage.com",
      "first_name": "Trevor",
      "last_name": "Kray"
    },
    "company": {
      "name": "Avantage",
      "id": 267,
      "url": "www.avantage.com",
      "created_at": "2015-01-14T17:26:43.410Z",
      "updated_at": "2015-03-05T19:54:14.628Z",
      "is_partner": true,
      "parent_id": null,
      "company_type": "partner",
      "partner_application_id": null,
      "address": {
        "street": "1055 W. Hastings St., Suite 300",
        "city": "Vancouver",
        "state": "BC",
        "country": "CA",
        "zip": "V6E 2E9",
        "phone": "(604) 685-1401"
      }
    },
    "product_lines": "Cost Transparency, Business Insights",
    "vertical_industries": "Healthcare Providers, Utilities"
  },
  "message": "OK"
}
```

This endpoint updates a specific Deal.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/deals/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Deal to update

# Users

## Get All Users

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  -s 'http://#{client}|.#{environment}|.test.partnerpath.net/api/users' -i
```

> The above command returns JSON structured like this:

```json
[
{
  "users": [
    {
      "id": 1112,
      "email": "wkihn@paypal.com",
      "job_function_id": null,
      "created_at": "2013-05-13T00:00:00.000Z",
      "updated_at": "2014-02-05T13:00:24.000Z",
      "first_name": "Wilfredo",
      "last_name": "Kihn",
      "title": "Senior Solutions Analyst",
      "company_id": 150,
      "company": {
        "name": "PayPal",
        "id": 150,
        "url": "http:\/\/paypal.com",
        "created_at": "2014-08-14T23:11:52.195Z",
        "updated_at": "2014-08-15T21:57:10.591Z",
        "is_partner": false,
        "parent_id": null,
        "company_type": null
      },
      "user_profile": {
        "id": 27,
        "user_id": 1112,
        "role_id": 5,
        "created_at": "2014-08-14T23:12:03.087Z",
        "updated_at": "2014-08-14T23:12:03.350Z",
        "accept_date": null
      }
    },
    {
      "id": 1090,
      "email": "jstark@paypal.com",
      "job_function_id": null,
      "created_at": "2013-01-19T00:00:00.000Z",
      "updated_at": "2013-12-04T19:53:19.000Z",
      "first_name": "Jerrold",
      "last_name": "Stark",
      "title": "Legacy Program Facilitator",
      "company_id": 150,
      "company": {
        "name": "PayPal",
        "id": 150,
        "url": "http:\/\/paypal.com",
        "created_at": "2014-08-14T23:11:52.195Z",
        "updated_at": "2014-08-15T21:57:10.591Z",
        "is_partner": false,
        "parent_id": null,
        "company_type": null
      },
      "user_profile": {
        "id": 5,
        "user_id": 1090,
        "role_id": 6,
        "created_at": "2014-08-14T23:12:00.234Z",
        "updated_at": "2014-08-14T23:12:00.256Z",
        "accept_date": null
      }
    },
    {
      "id": 1097,
      "email": "rstiedemann@cummeratamobile.com",
      "job_function_id": null,
      "created_at": "2012-10-30T00:00:00.000Z",
      "updated_at": "2013-02-14T21:21:23.000Z",
      "first_name": "Reuben",
      "last_name": "Stiedemann",
      "title": "Dynamic Applications Strategist",
      "company_id": 165,
      "company": {
        "name": "Cummerata Mobile",
        "id": 165,
        "url": "http:\/\/cummeratamobile.com",
        "created_at": "2014-08-14T23:11:53.909Z",
        "updated_at": "2014-08-14T23:12:27.294Z",
        "is_partner": true,
        "parent_id": null,
        "company_type": null
      },
      "user_profile": {
        "id": 12,
        "user_id": 1097,
        "role_id": 5,
        "created_at": "2014-08-14T23:12:01.115Z",
        "updated_at": "2014-08-14T23:12:01.136Z",
        "accept_date": null
      }
    },
    {
      "id": 1091,
      "email": "etorp@solutionscorp.com",
      "job_function_id": null,
      "created_at": "2012-12-22T00:00:00.000Z",
      "updated_at": "2013-11-18T12:50:05.000Z",
      "first_name": "Elena",
      "last_name": "Torp",
      "title": "Chief Communications Orchestrator",
      "company_id": 155,
      "company": {
        "name": "SolutionsCorp",
        "id": 155,
        "url": "http:\/\/solutionscorp.com",
        "created_at": "2014-08-14T23:11:52.803Z",
        "updated_at": "2014-08-18T23:01:24.727Z",
        "is_partner": true,
        "parent_id": null,
        "company_type": null
      },
      "user_profile": {
        "id": 6,
        "user_id": 1091,
        "role_id": 4,
        "created_at": "2014-08-14T23:12:00.361Z",
        "updated_at": "2014-08-14T23:12:00.383Z",
        "accept_date": null
      }
    },
    {
      "id": 1092,
      "email": "zzulauf@projectionsagency.com",
      "job_function_id": null,
      "created_at": "2012-01-24T00:00:00.000Z",
      "updated_at": "2014-08-07T22:03:27.000Z",
      "first_name": "Zachery",
      "last_name": "Zulauf",
      "title": "Corporate Data Technician",
      "company_id": 157,
      "company": {
        "name": "Projections Agency",
        "id": 157,
        "url": "http:\/\/projectionsagency.com",
        "created_at": "2014-08-14T23:11:53.014Z",
        "updated_at": "2014-08-14T23:12:27.675Z",
        "is_partner": true,
        "parent_id": null,
        "company_type": null
      },
      "user_profile": {
        "id": 7,
        "user_id": 1092,
        "role_id": 4,
        "created_at": "2014-08-14T23:12:00.490Z",
        "updated_at": "2014-08-14T23:12:00.510Z",
        "accept_date": null
      }
    },
    {
      "id": 1087,
      "email": "dtremblay@paypal.com",
      "job_function_id": null,
      "created_at": "2013-02-06T00:00:00.000Z",
      "updated_at": "2013-09-14T21:47:01.000Z",
      "first_name": "Dora",
      "last_name": "Tremblay",
      "title": "Lead Usability Agent",
      "company_id": 150,
      "company": {
        "name": "PayPal",
        "id": 150,
        "url": "http:\/\/paypal.com",
        "created_at": "2014-08-14T23:11:52.195Z",
        "updated_at": "2014-08-15T21:57:10.591Z",
        "is_partner": false,
        "parent_id": null,
        "company_type": null
      },
      "user_profile": {
        "id": 2,
        "user_id": 1087,
        "role_id": 6,
        "created_at": "2014-08-14T23:11:59.813Z",
        "updated_at": "2014-08-14T23:11:59.850Z",
        "accept_date": null
      }
    },
    {
      "id": 1088,
      "email": "twuckert@paypal.com",
      "job_function_id": null,
      "created_at": "2013-06-05T00:00:00.000Z",
      "updated_at": "2014-08-14T08:50:20.000Z",
      "first_name": "Titus",
      "last_name": "Wuckert",
      "title": "Forward Quality Representative",
      "company_id": 150,
      "company": {
        "name": "PayPal",
        "id": 150,
        "url": "http:\/\/paypal.com",
        "created_at": "2014-08-14T23:11:52.195Z",
        "updated_at": "2014-08-15T21:57:10.591Z",
        "is_partner": false,
        "parent_id": null,
        "company_type": null
      },
      "user_profile": {
        "id": 3,
        "user_id": 1088,
        "role_id": 7,
        "created_at": "2014-08-14T23:11:59.968Z",
        "updated_at": "2014-08-14T23:11:59.990Z",
        "accept_date": null
      }
    }
  ],
  "message": "OK"
}
]
```

This endpoint retrieves all users.

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/users`

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

## Get a Specific User

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  'http://#{client}|.#{environment}|.test.partnerpath.net/api/users/1092' -i
```

> The above command returns JSON structured like this:

```json
{
  "user": {
    "id": 1092,
    "email": "zzulauf@projectionsagency.com",
    "job_function_id": null,
    "created_at": "2012-01-24T00:00:00.000Z",
    "updated_at": "2014-08-07T22:03:27.000Z",
    "first_name": "Zachery",
    "last_name": "Zulauf",
    "title": "Corporate Data Technician",
    "company_id": 157,
    "company": {
      "name": "Projections Agency",
      "id": 157,
      "url": "http:\/\/projectionsagency.com",
      "created_at": "2014-08-14T23:11:53.014Z",
      "updated_at": "2014-08-14T23:12:27.675Z",
      "is_partner": true,
      "parent_id": null,
      "company_type": null
    },
    "user_profile": {
      "id": 7,
      "user_id": 1092,
      "role_id": 4,
      "created_at": "2014-08-14T23:12:00.490Z",
      "updated_at": "2014-08-14T23:12:00.510Z",
      "accept_date": null,
      "role_display": "Partner Admin"
    }
  },
  "message": "OK"
}
```
> Unless the User does not exist. In that case it returns JSON structured like this:

```json
{
  "contact": {
    "id": 8,
    "contact_type_id": 1,
    "first_name": "Ryann",
    "last_name": "Weimann",
    "title": "Dynamic Tactics Technician",
    "email": "millie@vonconnelly.com",
    "phone": "1-515-687-0854",
    "mobile": "1-415-556-7632",
    "company_id": null,
    "created_at": "2014-08-14T23:11:53.055Z",
    "updated_at": "2014-08-14T23:11:53.055Z",
    "contactable_type": "Company",
    "contactable_id": 157
  },
  "message": "OK"
}
```

This endpoint retrieves a specific user.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the User/Contact to retrieve

## Create a User

```shell
  curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X POST --data @buster.json 'http://demopath.test:3000/api/users'
```
> buster.json:

```
{
  "user": {
    "email": "kkool@thumper.com",
    "first_name": "Ken",
    "last_name": "Kool",
    "title": "King of Town",
    "company_id": 6868,
    "phone": "8003253535",
    "password": "P4rtn3rs!4ll",
    "password_confirmation": "P4rtn3rs!4ll",
    "user_profile": {
      "role_id": 5
    }
  }
}
```
> The above command returns JSON structured like this:

```json
{
  "user": {
    "id": 15575,
    "email": "kkool@thumper.com",
    "job_function_id": null,
    "first_name": "Ken",
    "last_name": "Kool",
    "title": "King of Town",
    "company_id": 6868,
    "phone": "",
    "account_confirmation_link": null,
    "password_reset_link": null,
    "account_confirmation_link_date": null,
    "password_reset_link_date": null,
    "active": true,
    "inactive_date": null,
    "created_at": "2016-07-27T21:17:41.541Z",
    "updated_at": "2016-07-27T21:17:41.541Z",
    "company": {
      "name": "Thumper",
      "id": 6868,
      "url": "http:\/\/www.thumper.com",
      "is_partner": true,
      "active": true,
      "company_type": "partner",
      "parent_id": null,
      "partner_application_id": null,
      "inactive_date": null,
      "deleted": false,
      "deleted_at": null,
      "deleted_by_user_id": null,
      "created_at": "2016-07-27T17:24:56.410Z",
      "updated_at": "2016-07-27T21:17:41.626Z"
    },
    "user_profile": {
      "id": 1751,
      "user_id": 15575,
      "role_id": 5,
      "created_at": "2016-07-27T21:17:41.547Z",
      "updated_at": "2016-07-27T21:17:41.547Z",
      "accept_date": null,
      "external_id": "",
      "sfdc_id": null
    }
  },
  "message": "OK"
}
```

This endpoint creates a specific User.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`POST http://#{client}|.#{environment}|.test.partnerpath.net/api/users`

## Update a Specific User

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"user": {"title": "Assistant to the Regional Manager"}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/users/1092'
```

> The above command returns JSON structured like this:

```json
{
  "user": {
    "id": 1092,
    "email": "zzulauf@projectionsagency.com",
    "job_function_id": null,
    "created_at": "2012-01-24T00:00:00.000Z",
    "updated_at": "2014-08-18T23:59:59.434Z",
    "first_name": "Zachery",
    "last_name": "Zulauf",
    "title": "Assistant to the Regional Manager",
    "company_id": 157,
    "company": {
      "name": "Projections Agency",
      "id": 157,
      "url": "http:\/\/projectionsagency.com",
      "created_at": "2014-08-14T23:11:53.014Z",
      "updated_at": "2014-08-18T23:59:59.587Z",
      "is_partner": true,
      "parent_id": null,
      "company_type": null
    },
    "user_profile": {
      "id": 7,
      "user_id": 1092,
      "role_id": 4,
      "created_at": "2014-08-14T23:12:00.490Z",
      "updated_at": "2014-08-14T23:12:00.510Z",
      "accept_date": null
    }
  },
  "message": "OK"
}
```

This endpoint updates a specific user.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

``PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the User to update

# PartnerApplications

## Get All Partner Applications

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  -s 'http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications' -i
```

> The above command returns JSON structured like this:

```json
[
{
  "partner_applications": [
    {
      "id": 1,
      "company_name": "PayPal",
      "domain_name": "paypal.com",
      "status": "Pending Approval",
      "company_type_id": null,
      "stock_symbol": null,
      "company_established_date": null,
      "total_annual_revenue_id": null,
      "number_of_customers_id": null,
      "percent_revenue_by": {
        "1": "",
        "2": "",
        "3": "",
        "4": "",
        "5": ""
      },
      "percent_sales_to": null,
      "number_employees_by": null,
      "info_competitors": null,
      "info_service_offerings": "",
      "info_programs": null,
      "info_expectations": "",
      "self_cotype_id": 3,
      "engagement_level_ids": [

      ],
      "product_line_ids": [

      ],
      "market_segment_ids": [

      ],
      "vertical_industry_ids": [

      ],
      "partner_request": null,
      "cogroup_id": null,
      "cotype_ids": null,
      "created_at": "2014-09-03T23:18:40.080Z",
      "updated_at": "2014-09-03T23:18:40.297Z",
      "parent_company_id": null,
      "approval_user_id": null,
      "url": null,
      "token": null,
      "address": {
        "id": 27,
        "street": "2211 N. First St.",
        "city": "San Jose",
        "state": "CT",
        "country": "US",
        "zip": "95131",
        "phone": "4089677217",
        "fax": "",
        "created_at": "2014-09-03T23:18:40.129Z",
        "updated_at": "2014-09-03T23:18:40.129Z",
        "addressable_type": "PartnerApplication",
        "addressable_id": 1,
        "latitude": null,
        "longitude": null
      },
      "contact": {
        "id": 27,
        "contact_type_id": 1,
        "first_name": "Stuart",
        "last_name": "Cohen",
        "title": "Manager",
        "email": "stcohen@paypal.com",
        "phone": "4089677217",
        "mobile": "4089677217",
        "company_id": null,
        "created_at": "2014-09-03T23:18:40.191Z",
        "updated_at": "2014-09-03T23:18:40.191Z",
        "contactable_type": "PartnerApplication",
        "contactable_id": 1
      },
      "geocoverage": {
        "id": 53,
        "coverable_id": 1,
        "coverable_type": "PartnerApplication",
        "geography_ids": [
          "2"
        ],
        "region_ids": [

        ],
        "country_codes": [

        ],
        "created_at": "2014-09-03T23:18:40.281Z",
        "updated_at": "2014-09-03T23:18:40.281Z"
      }
    },
    {
      "id": 4,
      "company_name": "Stu Test 5",
      "domain_name": "snakeskin.com",
      "status": "Pending Approval",
      "company_type_id": null,
      "stock_symbol": null,
      "company_established_date": null,
      "total_annual_revenue_id": null,
      "number_of_customers_id": null,
      "percent_revenue_by": null,
      "percent_sales_to": null,
      "number_employees_by": null,
      "info_competitors": null,
      "info_service_offerings": null,
      "info_programs": null,
      "info_expectations": null,
      "self_cotype_id": 1,
      "engagement_level_ids": [

      ],
      "product_line_ids": null,
      "market_segment_ids": null,
      "vertical_industry_ids": [
        "5"
      ],
      "partner_request": null,
      "cogroup_id": null,
      "cotype_ids": [

      ],
      "created_at": "2014-10-30T22:25:16.948Z",
      "updated_at": "2014-11-11T19:30:58.621Z",
      "parent_company_id": null,
      "approval_user_id": null,
      "url": null,
      "token": null,
      "address": {
        "id": 30,
        "street": "2211 N. First St.",
        "city": "San Jose",
        "state": "CA",
        "country": "US",
        "zip": "95131",
        "phone": "4089677217",
        "fax": "",
        "created_at": "2014-10-30T22:25:17.001Z",
        "updated_at": "2014-11-11T19:30:58.533Z",
        "addressable_type": "PartnerApplication",
        "addressable_id": 4,
        "latitude": 32.4063875,
        "longitude": -110.9612216
      },
      "contact": {
        "id": 30,
        "contact_type_id": 1,
        "first_name": "Stuart",
        "last_name": "Cohen",
        "title": "sales",
        "email": "stcohen@paypal.com",
        "phone": "4089677217",
        "mobile": "4089677217",
        "company_id": null,
        "created_at": "2014-10-30T22:25:17.065Z",
        "updated_at": "2014-10-30T22:25:17.065Z",
        "contactable_type": "PartnerApplication",
        "contactable_id": 4
      },
      "geocoverage": {
        "id": 92,
        "coverable_id": 4,
        "coverable_type": "PartnerApplication",
        "geography_ids": [
          "6",
          "9"
        ],
        "region_ids": [

        ],
        "country_codes": [

        ],
        "created_at": "2014-10-30T22:25:17.130Z",
        "updated_at": "2014-11-11T19:30:05.952Z"
      },
      "custom": {
        "id": 9,
        "fields": {
          "custom_paypal_company_description": "this is my company",
          "custom_paypal_processing_volume": "3",
          "custom_paypal_merchants": "2"
        },
        "customizable_id": 4,
        "customizable_type": "PartnerApplication",
        "created_at": "2014-10-30T22:25:16.920Z",
        "updated_at": "2014-10-30T22:25:17.177Z"
      },
      "contract": {
        "id": 1,
        "contractable_id": 4,
        "contractable_type": "PartnerApplication",
        "fee": null,
        "start_date": null,
        "end_date": null,
        "auto_start_date": null,
        "auto_end_date": null,
        "created_at": "2014-10-30T22:26:52.637Z",
        "updated_at": "2014-10-30T22:26:52.637Z"
      }
    }
  ],
  "message": "OK"
}
]
```

This endpoint retrieves all partner applications.

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications`

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

## Get a Specific Partner Application

```shell
curl -H 'X-API-Version: 1' -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -w '\nLookup time:\t%{time_namelookup}\nTotal time:\t%{time_total}\n' \
  'http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/4' -i
```

> The above command returns JSON structured like this:

```json
{
  "partner_application": {
    "id": 4,
    "company_name": "Stu Test 5",
    "domain_name": "snakeskin.com",
    "status": "Pending Approval",
    "company_type_id": null,
    "stock_symbol": null,
    "company_established_date": null,
    "total_annual_revenue_id": null,
    "number_of_customers_id": null,
    "percent_revenue_by": null,
    "percent_sales_to": null,
    "number_employees_by": null,
    "info_competitors": null,
    "info_service_offerings": null,
    "info_programs": null,
    "info_expectations": null,
    "self_cotype_id": 1,
    "engagement_level_ids": [

    ],
    "product_line_ids": null,
    "market_segment_ids": null,
    "vertical_industry_ids": [
      "5"
    ],
    "partner_request": null,
    "cogroup_id": null,
    "cotype_ids": [

    ],
    "created_at": "2014-10-30T22:25:16.948Z",
    "updated_at": "2014-11-11T19:30:58.621Z",
    "parent_company_id": null,
    "approval_user_id": null,
    "url": null,
    "token": null,
    "address": {
      "id": 30,
      "street": "2211 N. First St.",
      "city": "San Jose",
      "state": "CA",
      "country": "US",
      "zip": "95131",
      "phone": "4089677217",
      "fax": "",
      "created_at": "2014-10-30T22:25:17.001Z",
      "updated_at": "2014-11-11T19:30:58.533Z",
      "addressable_type": "PartnerApplication",
      "addressable_id": 4,
      "latitude": 32.4063875,
      "longitude": -110.9612216
    },
    "contact": {
      "id": 30,
      "contact_type_id": 1,
      "first_name": "Stuart",
      "last_name": "Cohen",
      "title": "sales",
      "email": "stcohen@paypal.com",
      "phone": "4089677217",
      "mobile": "4089677217",
      "company_id": null,
      "created_at": "2014-10-30T22:25:17.065Z",
      "updated_at": "2014-10-30T22:25:17.065Z",
      "contactable_type": "PartnerApplication",
      "contactable_id": 4
    },
    "geocoverage": {
      "id": 92,
      "coverable_id": 4,
      "coverable_type": "PartnerApplication",
      "geography_ids": [
        "6",
        "9"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2014-10-30T22:25:17.130Z",
      "updated_at": "2014-11-11T19:30:05.952Z"
    },
    "custom": {
      "id": 9,
      "fields": {
        "custom_paypal_company_description": "this is my company",
        "custom_paypal_processing_volume": "3",
        "custom_paypal_merchants": "2"
      },
      "customizable_id": 4,
      "customizable_type": "PartnerApplication",
      "created_at": "2014-10-30T22:25:16.920Z",
      "updated_at": "2014-10-30T22:25:17.177Z"
    },
    "contract": {
      "id": 1,
      "contractable_id": 4,
      "contractable_type": "PartnerApplication",
      "fee": null,
      "start_date": null,
      "end_date": null,
      "auto_start_date": null,
      "auto_end_date": null,
      "created_at": "2014-10-30T22:26:52.637Z",
      "updated_at": "2014-10-30T22:26:52.637Z"
    }
  },
  "message": "OK"
}
```

This endpoint retrieves a specific partner application.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`GET http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Partner Application to retrieve


## Update a Specific Partner Application

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"partner_application": {"market_segment_ids": "Hardware Offering, Hosting Services, Training Offering", "domain_name": "snakeskin.com", "url": "http://www.snakeskin.com"}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/4'
```

> The above command returns JSON structured like this:

```json
{
  "partner_application": {
    "id": 4,
    "company_name": "Stu Test 5",
    "domain_name": "snakeskin.com",
    "status": "Approved Pending Partner Acceptance",
    "company_type_id": null,
    "stock_symbol": null,
    "company_established_date": null,
    "total_annual_revenue_id": null,
    "number_of_customers_id": null,
    "percent_revenue_by": null,
    "percent_sales_to": null,
    "number_employees_by": null,
    "info_competitors": null,
    "info_service_offerings": null,
    "info_programs": null,
    "info_expectations": null,
    "self_cotype_id": 1,
    "engagement_level_ids": [

    ],
    "product_line_ids": null,
    "market_segment_ids": "Hardware Offering, Hosting Services, Training Offering",
    "vertical_industry_ids": "",
    "partner_request": null,
    "cogroup_id": "Gold",
    "cotype_ids": "Solution Provider - Online, Systems Integrator - Online",
    "created_at": "2014-10-30T22:25:16.948Z",
    "updated_at": "2014-12-16T00:49:15.764Z",
    "parent_company_id": null,
    "approval_user_id": null,
    "url": "http:\/\/www.snakeskin.com",
    "token": null,
    "decline_reason_id": null,
    "decline_comment": null,
    "address": {
      "id": 30,
      "street": "2211 N. First St.",
      "city": "San Jose",
      "state": "AZ",
      "country": "US",
      "zip": "95131",
      "phone": "4089677217",
      "fax": "",
      "created_at": "2014-10-30T22:25:17.001Z",
      "updated_at": "2014-10-30T22:25:17.555Z",
      "addressable_type": "PartnerApplication",
      "addressable_id": 4,
      "latitude": 32.4063875,
      "longitude": -110.9612216
    },
    "contact": {
      "id": 30,
      "contact_type_id": 1,
      "first_name": "Stuart",
      "last_name": "Cohen",
      "title": "sales",
      "email": "stcohen@paypal.com",
      "phone": "4089677217",
      "mobile": "4089677217",
      "company_id": null,
      "created_at": "2014-10-30T22:25:17.065Z",
      "updated_at": "2014-10-30T22:25:17.065Z",
      "contactable_type": "PartnerApplication",
      "contactable_id": 4
    },
    "geocoverage": {
      "id": 92,
      "coverable_id": 4,
      "coverable_type": "PartnerApplication",
      "geography_ids": [
        "6"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2014-10-30T22:25:17.130Z",
      "updated_at": "2014-12-16T00:49:15.752Z"
    },
    "custom": {
      "id": 9,
      "fields": {
        "custom_paypal_company_description": "this is my company",
        "custom_paypal_processing_volume": "3",
        "custom_paypal_merchants": "2"
      },
      "customizable_id": 4,
      "customizable_type": "PartnerApplication",
      "created_at": "2014-10-30T22:25:16.920Z",
      "updated_at": "2014-10-30T22:25:17.177Z"
    },
    "contract": {
      "id": 7,
      "contractable_id": 4,
      "contractable_type": "PartnerApplication",
      "fee": null,
      "start_date": "2014-11-17",
      "end_date": "2014-12-12",
      "auto_start_date": null,
      "auto_end_date": null,
      "created_at": "2014-11-18T20:15:19.663Z",
      "updated_at": "2014-11-18T20:15:19.663Z",
      "signatory_name": null,
      "signatory_email": null,
      "agreements": [
        {
          "name": "NA2014 Program",
          "external_agreement_id": "12345",
          "agreement_type": "Standard"
        }
      ]
    }
  },
  "message": "OK"
}
```

This endpoint updates a specific partner application.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Partner Application to update

## Reject or decline a Specific Partner Application

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
  -H 'Authorization: Token access_token="thepartnerpathtoken"' \
  -X PATCH --data '{"partner_application": {"decline_type": "Merchant", "decline_comment": "Better luck next time"}}' 'http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/reject/11'
```

> The above command returns JSON structured like this:

```json
{
  "partner_application": {
    "id": 11,
    "company_name": "Stanley Tools",
    "domain_name": "stanleytools.com",
    "status": "Application Denied",
    "company_type_id": null,
    "stock_symbol": null,
    "company_established_date": null,
    "total_annual_revenue_id": null,
    "number_of_customers_id": null,
    "percent_revenue_by": null,
    "percent_sales_to": null,
    "number_employees_by": null,
    "info_competitors": null,
    "info_service_offerings": null,
    "info_programs": null,
    "info_expectations": null,
    "self_cotype_id": 1,
    "engagement_level_ids": [

    ],
    "product_line_ids": null,
    "market_segment_ids": null,
    "vertical_industry_ids": "",
    "partner_request": null,
    "cogroup_id": "Gold",
    "cotype_ids": "",
    "created_at": "2014-12-03T23:28:34.485Z",
    "updated_at": "2015-02-24T16:36:20.116Z",
    "parent_company_id": null,
    "approval_user_id": null,
    "url": "http:\/\/www.stanleytools.com\/",
    "token": "e355304ec1fc9e60",
    "decline_comment": "Better luck next time",
    "address": {
      "id": 43,
      "street": "5 Main St.",
      "city": "New City",
      "state": "AL",
      "country": "US",
      "zip": "22222",
      "phone": "4089677217",
      "fax": "4082223333",
      "created_at": "2014-12-03T23:28:34.493Z",
      "updated_at": "2014-12-03T23:28:36.200Z",
      "addressable_type": "PartnerApplication",
      "addressable_id": 11,
      "latitude": 28.4021396,
      "longitude": 77.3234737
    },
    "contact": {
      "id": 43,
      "contact_type_id": 1,
      "first_name": "Stanley",
      "last_name": "Tools",
      "title": "President",
      "email": "joestanley@stanleytools.com",
      "phone": "214-333-5555",
      "mobile": "433-333-3333",
      "company_id": null,
      "created_at": "2014-12-03T23:28:34.517Z",
      "updated_at": "2015-02-24T16:36:04.166Z",
      "contactable_type": "PartnerApplication",
      "contactable_id": 11
    },
    "geocoverage": {
      "id": 130,
      "coverable_id": 11,
      "coverable_type": "PartnerApplication",
      "geography_ids": [
        "6"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2014-12-03T23:28:34.533Z",
      "updated_at": "2015-02-24T16:36:20.106Z"
    },
    "custom": {
      "id": 35,
      "fields": {
        "custom_paypal_company_description": "We Make tools",
        "custom_paypal_processing_volume": "2",
        "custom_paypal_merchants": "3",
        "custom_paypal_application_approver": "1346",
        "custom_paypal_campaign": "",
        "custom_paypal_product_expertise": "4"
      },
      "customizable_id": 11,
      "customizable_type": "PartnerApplication",
      "created_at": "2014-12-03T23:28:34.455Z",
      "updated_at": "2015-02-24T16:36:04.405Z"
    },
    "contract": {
      "id": 19,
      "contractable_id": 11,
      "contractable_type": "PartnerApplication",
      "fee": null,
      "start_date": "2014-12-04",
      "end_date": "2014-12-17",
      "auto_start_date": null,
      "auto_end_date": null,
      "created_at": "2014-12-03T23:28:34.570Z",
      "updated_at": "2014-12-05T21:15:21.402Z",
      "signatory_name": null,
      "signatory_email": null,
      "agreements": [

      ]
    },
    "decline_type": "Merchant"
  },
  "message": "OK"
}
```

This endpoint rejects or declines a specific partner application.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/reject/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Partner Application to reject or decline

## Approve a Specific Partner Application

```shell
curl --dump-header - -H "Content-Type: application/json" -H 'X-API-Version: 1' \
-H 'Authorization: Token access_token="337a966a061ed2beb61f5172772162a8"' \
-X PUT --data '{"partner_application": {"contracts":[ {"name": "NA2014 Program", "title": "Special NA2014 Program", "type": "Standard", "start_date" : "2015-01-13", "end_date" : "2017-01-13", "external_id" : "12345"}]}}' \
'http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/approve/35'
```

> The above command returns JSON structured like this:

```json
{
  "partner_application": {
    "id": 35,
    "company_name": "Cretaceous Creatures",
    "domain_name": "cretaceouscreatures.com",
    "status": "Approved Pending Partner Acceptance",
    "company_type_id": null,
    "stock_symbol": null,
    "company_established_date": null,
    "total_annual_revenue_id": null,
    "number_of_customers_id": null,
    "percent_revenue_by": null,
    "percent_sales_to": null,
    "number_employees_by": null,
    "info_competitors": null,
    "info_service_offerings": null,
    "info_programs": null,
    "info_expectations": null,
    "self_cotype_id": 3,
    "engagement_level_ids": null,
    "product_line_ids": null,
    "market_segment_ids": null,
    "vertical_industry_ids": "",
    "partner_request": null,
    "cogroup_id": "Registered",
    "cotype_ids": "",
    "created_at": "2015-01-13T16:02:53.885Z",
    "updated_at": "2015-01-13T16:49:09.322Z",
    "parent_company_id": null,
    "approval_user_id": null,
    "url": "http:\/\/cretaceouscreatures.com",
    "token": "92e64c588c08b46c",
    "decline_reason_id": null,
    "decline_comment": null,
    "address": {
      "id": 84,
      "street": "13 Elm Street",
      "city": "Seattle",
      "state": "WA",
      "country": "US",
      "zip": "98101",
      "phone": "2063253535",
      "fax": "",
      "created_at": "2015-01-13T16:02:53.960Z",
      "updated_at": "2015-01-13T16:02:59.133Z",
      "addressable_type": "PartnerApplication",
      "addressable_id": 35,
      "latitude": 47.5936535,
      "longitude": -122.3841674
    },
    "contact": {
      "id": 84,
      "contact_type_id": 1,
      "first_name": "Marshawn",
      "last_name": "Lynch",
      "title": "Beast",
      "email": "marshawn@cretaceouscreatures.com",
      "phone": "2063253535",
      "mobile": "2063253535",
      "company_id": null,
      "created_at": "2015-01-13T16:02:54.019Z",
      "updated_at": "2015-01-13T16:02:54.019Z",
      "contactable_type": "PartnerApplication",
      "contactable_id": 35
    },
    "geocoverage": {
      "id": 180,
      "coverable_id": 35,
      "coverable_type": "PartnerApplication",
      "geography_ids": [
        "6"
      ],
      "region_ids": [

      ],
      "country_codes": [

      ],
      "created_at": "2015-01-13T16:02:54.068Z",
      "updated_at": "2015-01-13T16:49:09.304Z"
    },
    "custom": {
      "id": 73,
      "fields": {
        "custom_paypal_company_description": "Product with value",
        "custom_paypal_processing_volume": "3",
        "custom_paypal_merchants": "3",
        "custom_paypal_campaign": ""
      },
      "customizable_id": 35,
      "customizable_type": "PartnerApplication",
      "created_at": "2015-01-13T16:02:53.856Z",
      "updated_at": "2015-01-13T16:02:54.104Z"
    },
    "contract": {
      "id": 78,
      "contractable_id": 35,
      "contractable_type": "PartnerApplication",
      "fee": null,
      "start_date": null,
      "end_date": null,
      "auto_start_date": null,
      "auto_end_date": null,
      "created_at": "2015-01-13T16:02:54.123Z",
      "updated_at": "2015-01-13T16:02:54.123Z",
      "signatory_name": null,
      "signatory_email": null,
      "agreements": [
        {
          "name": "NA2014 Program",
          "external_agreement_id": "12345",
          "agreement_type": "Standard",
          "title": "Special NA2014 Program"
        }
      ]
    }
  },
  "message": "OK"
}
```

This endpoint approves a specific partner application.

<aside class="success">Message - OK</aside>
<aside class="warning">If you're not using an administrator API key this operation will return 403 Forbidden.</aside>

### HTTP Request

`PUT http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/approve/<ID>`

`PATCH http://#{client}|.#{environment}|.test.partnerpath.net/api/partner_applications/approve/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Partner Application to approve


