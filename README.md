# Three-AUVs-acoustic-communication-data
Ground truth AUV data collected Chesapeake bay area

The .mat data is constructed as follows:


For all AUVs positions, we use ECEF(Earth-Centered, Earth-Fixed) coordinates with WGS84 ellipsoid constants a = 6378137 and e = 8.1819190842622e-2

X = ECEF X-coordinate(meters)
Y = ECEF Y-coordinate(meters)
Z = ECEF Z-coordinate(meters)

# AUV A,B,C trajectories in ECEF
AUV_A_locArray_1.mat / AUV_B_locArray_1.mat / AUV_C_locArray_1.mat record three AUV ground truth positions in ECEF coordinates
.mat data file has three columns:
| X | Y | Z |


# AUV A,B,C successful communications
A_send_B_rece_suc_pack_1.mat / A_send_C_rece_suc_pack_1.mat / B_send_A_rece_suc_pack_1.mat / B_send_C_rece_suc_pack_1.mat / C_send_A_rece_suc_pack_1.mat / C_send_B_rece_suc_pack_1.mat record successful communication events. For exmaple A_send_B_rece_suc_pack_1.mat records all successful communications including positions sending from AUV A to AUV B. Sending time is unix time in seconds.

.mat data file has ten columns:

| sending_time_unix | receiving_time_unix | sending_position_X | sending_position_Y | sending_position_Z | receiving_position_X | receiving_position_Y | receiving_position_Z | distance | label |

where distance(meters) is the ground truth distance between sending and receiving AUV when event happens and label = 1 represents successful event.



# AUV A,B,C unsuccessful communications
A_send_B_rece_unsuc_pack_1.mat / A_send_C_rece_unsuc_pack_1.mat / B_send_A_rece_unsuc_pack_1.mat / B_send_C_rece_unsuc_pack_1.mat / C_send_A_rece_unsuc_pack_1.mat / C_send_B_rece_unsuc_pack_1.mat record unsuccessful communication events. For exmaple A_send_B_rece_unsuc_pack_1.mat records all unsuccessful communications including positions sending from AUV A to AUV B.

.mat data file has nine columns:

| sending_time_unix | sending_position_X | sending_position_Y | sending_position_Z | receiving_position_X | receiving_position_Y | receiving_position_Z | distance | label |

where distance(meters) is the ground truth distance between sending and receiving AUV when event happens and label = 0 represents unsuccessful event.



