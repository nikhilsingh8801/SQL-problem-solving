Football World Cup Group Stage Points Calculator

Task: SQL Problem solving

Problem Description
This SQL task is about calculating the total points each team has earned in the group stage of the Football World Cup based on match results.

You are given two tables:

1. teams Table

Represents all teams participating in the World Cup:

Column Name	Type	Description
team_id	INT	Primary key, unique ID for each team
team_name	VARCHAR(50)	Name of the team
2. matches Table

Represents all matches played in the group stage:

Column Name	Type	Description
match_id	INT	Primary key, unique ID for each match
host_team	INT	Team ID of the home team
guest_team	INT	Team ID of the visiting team
host_goals	INT	Goals scored by the home team
guest_goals	INT	Goals scored by the visiting team

Note: Teams are represented by their team_id. No team plays against itself.

Scoring Rules

Points are awarded based on match results:

Win: 3 points

Draw: 1 point

Loss: 0 points

Objective

Write an SQL query to compute the total points for each team after all matches and generate a ranking:

Columns to return: team_id, team_name, num_points

Sort by num_points in descending order.

In case of ties, sort by team_id in ascending order.

Sample Input
teams Table
team_id	team_name
10	Give
20	Never
30	You
40	Up
50	Gonna
matches Table
match_id	host_team	guest_team	host_goals	guest_goals
1	30	20	1	0
2	10	20	1	2
3	20	50	2	2
4	10	30	1	0
5	30	50	0	1
Expected Output
team_id	team_name	num_points
20	Never	4
50	Gonna	4
10	Give	3
30	You	3
40	Up	0
