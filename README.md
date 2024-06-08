#### 2024-06-08 

## Overview

This README file provides information about the list of cryptocurrency pump-and-dump events used in Ardia and Bluteau (2024), **Twitter and cryptocurrency pump-and-dumps**. [https://doi.org/10.2139/ssrn.4703467](https://doi.org/10.2139/ssrn.4703467)

By using the data, you agree to the following rules:

- You must cite the paper in working papers and published papers that use the data.
- You must place the [DOI](https://doi.org/10.5281/zenodo.10459612) of this data repository in a footnote to help others find it.
- You assume all risk for the use of the code.

## Data Availability and Provenance Statements

To assemble a comprehensive dataset, we initially compiled a list of approximately 100 pump-and-dump groups sourced from various forums on platforms such as Reddit and Discord. Additionally, we consulted websites that curate lists of cryptocurrency Telegram channels. Subsequently, we conducted an extensive search within the messages of these groups to identify links to other relevant groups, thereby expanding our list to encompass more than a hundred distinct groups.

The Telegram API, which is publicly accessible, facilitated downloading all messages from the groups or channels we had subscribed to or joined. Consequently, we extracted all messages along with their corresponding publication dates. To detect group-specific patterns, we implemented keyword searches within user conversations. Our data collection focuses exclusively on events occurring on the Binance exchange using the Bitcoin (BTC) trading pair. Moreover, we exclude events related to Dogecoin, Litecoin, Ethereum, and Cardano, as their widespread popularity posed challenges. In total, our dataset comprises 1,160 pump-and-dump events.

A pump-and-dump event can be classified as either successful or unsuccessful. Our strategy to identify successful events and determine the precise start time of an event involves two steps. First, we ascertain the success of an event. For each event, we collect volume data for one day before and one day after the event. Subsequently, we aggregate the minute-by-minute data into five-minute intervals, with the event minute serving as the starting point. If the volume within the five-minute interval encompassing the event ranks among the top three highest five-minute volumes over the two-day period (equating to 0.001\% of all observations), we classify the event as successful. The minute with the highest volume is defined as the pump date.

## List of events

We provide the list of events in the file `list_pd_events.csv` located in the folder `data`. Each event contains the following information:

| Date | Channel | Currency | Exchange | success | pump_date |

## References

Ardia D., Bluteau, K., 2024. Twitter and cryptocurrency pump-and-dumps. https://doi.org/10.2139/ssrn.4703467
