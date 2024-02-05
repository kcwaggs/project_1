Potential endpoints: PlayerDashboardByGeneralSplits
PlayerCareerStats
PlayerCareerByCollegeRollup
PlayerCareerByCollege
FranchisePlayers
resource: https://www.kaggle.com/datasets/bme3412/nba-player-stats-20002020-seasons?resource=download
another: https://www.kaggle.com/datasets/justinas/nba-players-data

I tried running the code below but it kept timing out due to the volume of data and rate limits for the API: 
    import time

    # Fetch common player info for all player IDs
    selected_players_df = pd.DataFrame()

    for player_id in all_players.index:
        common_p_info = commonplayerinfo.CommonPlayerInfo(player_id=str(player_id))
        common_p_info_df = common_p_info.get_data_frames()[0]

        print(f"Checking player_id: {player_id}")
        print(common_p_info_df[['DISPLAY_FIRST_LAST', 'FROM_YEAR', 'TO_YEAR']])

        # Additional debug information
        print(f"Unique FROM_YEAR values: {common_p_info_df['FROM_YEAR'].unique()}")
        print(f"Unique TO_YEAR values: {common_p_info_df['TO_YEAR'].unique()}")

        # Check if the player had any active years between 2000 and 2020
        if any((common_p_info_df['TO_YEAR'] >= 2000) & (common_p_info_df['FROM_YEAR'] <= 2020)):
            # Append the player information to the new DataFrame
            selected_players_df = pd.concat([selected_players_df, common_p_info_df])

        # Introduce a delay of 1 second between API requests
        time.sleep(1)

    # Save the DataFrame to a new CSV file
    selected_players_df.to_csv("resources/selected_players_2000_2020.csv", index=False)