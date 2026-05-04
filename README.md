# Payment-Failure-Reason-Classification

Project Overview

Digital payment platforms process millions of transactions every day. When a transaction fails, the failure may occur for different reasons such as insufficient funds, bank server outages, incorrect authentication, network instability, fraud risk triggers, or merchant configuration errors. In many real systems, users only see a generic message such as “Transaction Failed”. However, payment companies and financial institutions need to understand the exact reason for failure in order to improve user experience, reduce operational costs, and route issues to the correct operational teams. In this project, students will build a multi■class classification model that predicts the most likely reason for a payment failure using transaction metadata, device telemetry, network signals, and behavioral indicators.

Problem Statement

Given a dataset of failed payment transactions, build a machine learning model that predicts the single most likely failure reason for each transaction. Each record belongs to exactly one class representing the root cause of the failure.

Target Classes

Failure Classes

INSUFFICIENT_FUNDS

BANK_SERVER_DOWN

PIN_OR_OTP_FAILED

LIMIT_EXCEEDED

NETWORK_TIMEOUT

SUSPECTED_FRAUD

INVALID_VPA_OR_CARD

MERCHANT_CONFIGURATION_ISSUE

Data Dictionary

Column Description

txn_id Unique transaction identifier

user_id Unique identifier for the user initiating payment

merchant_id Unique identifier for merchant receiving payment

payment_method Type of payment used (UPI, Card, Wallet)amount Transaction amount

merchant_category Business category of the merchant

is_international Flag indicating international transaction

payer_bank Bank of the payer

payee_bank Bank of the receiver

issuer_type Type of issuing institution

device_type Device used for transaction

os_version_major Operating system version of device

app_version_major Payment application version

is_rooted_or_jailbroken Device security indicator

sim_operator Mobile network operator

network_type Connection type such as WIFI or mobile data

latency_ms Network latency in milliseconds

packet_loss_pct Network packet loss percentage

signal_strength_dbm Mobile signal strength

avg_txn_amount_30d Average transaction amount over last 30 days

txn_count_24h Number of transactions performed in last 24 hours

failed_txn_count_1h Number of failed attempts in last hour

chargeback_flag_180d Chargeback history indicator

account_age_days Age of user account

daily_limit_remaining Remaining transaction limit for the day

available_balance_est Estimated available balance

velocity_score Indicator of transaction burst activity

risk_score Fraud risk score

geo_distance_km_from_usual Distance from typical transaction location

txn_hour Hour of transaction

day_of_week Day of week

is_night_txn Indicator for night transactions

merchant_failure_rate_1h Failure rate for merchant in last hour

bank_failure_rate_1h Failure rate for bank in last hour

failure_reason Target variable representing failure class
