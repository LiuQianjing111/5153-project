# 5153-project
#1. Project Overview

Purpose: Predict Flight Delay and evaluate the model by confusion martrix

#2. Data Description

Data set depicts US domestic flights in 2018 comprising of 300000 rows × 28 columns. df = pd.read_csv("2018.csv", nrows=300000)

Content: FL_DATE: Airline Identifier

OP_CARRIER Flight Number

OP_CARRIER_F

L_NUM Starting Airport Code

ORIGIN Destination Airport Code

DEST Planned Departure Time

CRS_DEP_TIM

E Actual Departure Time

DEP_TIME Total Delay on Departure in minutes

DEP_DELAY The time duration elapsed between departure from the origin airport gate and wheels off

TAXI_OUT The time point that the aircraft's wheels leave the ground

WHEELS_OFF The time point that the aircraft's wheels touch on the ground

WHEELS_ON The time duration elapsed between wheels-on and gate arrival at the destination airport

TAXI_IN Planned arrival time

CRS_ARR_TIME Actual Arrival Time

ARR_TIME Total Delay on Arrival in minutes

ARR_DELAY Flight Cancelled (1 = cancelled)

CANCELLED Reason for Cancellation of flight: A - Airline/Carrier; B - Weather; C - National Air System; D - Security

CANCELLATIO

N_CODE Aircraft landed on airport that out of schedule

DIVERTED Planned time amount needed for the flight trip

CRS_ELAPSED

_TIME AIR_TIME+TAXI_IN+TAXI_OUT

ACTUAL_ELAP

SED_TIME The time duration between wheels_off and wheels_on time

AIR_TIME Distance between two airports

DISTANCE Delay caused by the airline in minutes

CARRIER_DEL

AY Delay caused by weather

WEATHER_DEL

AY Delay caused by air system

NAS_DELAY Delay caused by security

SECURITY_DEL

AY Delay caused by aircraft

LATE_AIRCRAFAirline Identifier

#Preprocessing:

One Hot Encoding:

Numerical Columns :'CRS_ARR_TIME', 'CRS_ELAPSED_TIME', 'DISTANCE', 'DAY_OF_MONTH'

Categorical Columns :'OP_CARRIER', 'DAY_OF_WEEK', 'IS_WEEKEND', 'IS_PUBLIC_HOLIDAY', 'IS_EVE_PUBLIC_HOLIDAY', 'ORIGIN', 'DEST'

Target :‘CLASSIFICATION’


#Train Test Split and SMOTE to Deal with Imbalanced data:

X is df_processed without ‘CLASSIFICATION’

Y is ‘CLASSIFICATION’ column in df_processed

