# Native Analytics

Altis Analytics is only available to Accelerate and Enterprise tier customers.

Altis Analytics provides a built in tool for tracking and analyzing user behavior across the site in real time. It is enabled by default but can be switched off via the configuration file:

```json
{
	"extra": {
		"altis": {
			"modules": {
				"analytics": {
					"native": false
				}
			}
		}
	}
}
```

Analytics data is stored in an S3 data lake and delivered to Elasticsearch where it is 1-5 minutes behind real-time.

The data is queried from Elasticsearch in the application providing a powerful query language with filtering and aggregations for collecting statistics and other metrics.

Altis Analytics can power features such as popular posts widgets, personalisation and A/B tests.

## Dashboards

By default Altis Analytics replaces the default WordPress dashboard with an overview of your best performing content.

If needed you can switch this off via the `dashboard` config option like so:

```json
{
	"extra": {
		"altis": {
			"modules": {
				"analytics": {
					"dashboard": false
				}
			}
		}
	}
}
```

Altis also provides a more detailed analytics view and insights page under the main Dashboard menu item in the admin.

## Data Structure and APIs

The highly flexible analytics data set is the engine behind [audiences](./audiences.md), and the [Altis Optimization Framework](../optimization-framework/README.md).

[Learn about the available APIs and the data structure in detail here](./api/README.md), and [learn about the different ways you can integrate analytics data with external services here](./api/data-export.md).

Altis also includes native integration for Segment.com, which when activated pushes analytics data to Segment for further tracking and analysis. [Learn about the Segment integration for Altis Analytics here](./api/integrations/segment.md).

## Optimization Framework

[Altis Optimization Framework](../optimization-framework/) is a flexible and extensive framework that enables Content Optimization through [Personalization](../optimization-framework/personalization.md) and [A/B tests](../optimization-framework/ab-testing.md), the features that power [Altis Experience Blocks](../experience-blocks.md).

## Audiences

[Audiences are a powerful tool](./audiences.md) for driving personalisation and gaining insights through testing and reporting.

## Privacy

[Discover how Altis helps to respect your visitor's privacy](./privacy.md) by helping you control how long to keep data for and learning how to process analytics data for long term storage.
