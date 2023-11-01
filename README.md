# Group 4 MIST Group Project 1:

# Team Name:
29704 Group 4

# Team Members:
Ryan Dean: [@RDean45](https://github.com/RDean45)

Ryan Kelly: [@Rjk4133](https://github.com/Rjk4133)

Cameron Smith: [@camjshmitt](https://github.com/camjshmitt)

Wyatt Smith: [@wsmith1287 ](https://github.com/wsmith1287)

Mattie Garett: [@MatGar22](https://github.com/MatGar22)

Lilly Wood: [@lillywood21](https://github.com/lillywood1)

# Problem Description:

The problem that we are trying to solve has to do with the creation of a working database that consolidates data for a soccer club into a functioning model. The main entity that comprises this data and the model is the Team entity which is made up of the different teams that comprise the soccer club and includes information such as their team name and where their home field is. In addition to this, we have other entities such as data on the players that comprise these teams, the statistics for each of these players, the coaching staff that make up the soccer club, and much more. In addition to a working model, we hope to build many working queries that provide data to possible stakeholders of the soccer club to make well informed complex decisions regarding the clubs activities. With this complex data model and the many different queries we hope to deliver working data that can be used by the soccer club to operate at an increased efficiency level and deliver better value to its stakeholders.

# Data Model:
Our model is structured like a football (soccer) academy. The Teams entity represents the information stored about each of the different teams in the club including the team ID, the team name, the team’s home field and more. Teams have many matches, which is shown by the one to many identifying relationship between Teams and Teams Have Matches. Teams also have head coaches which is represented by the one to one non identifying relationship between Teams and the entity Coaching Staff. Teams have many coaches which is shown by the one to many non identifying relationship between Teams and Coaching Staff. Teams may also have many sponsors which is represented by the one to many identifying relationship between Teams and the Teams Have Sponsors entity. Teams have many players which is shown by the one to many non identifying relationship between Teams and Player Information. Teams also have captains which are represented by the one to one non identifying relationship between Teams and Player Information.


Player Information stores data like the player’s player ID, the player’s first and last name, their age and much more. Players have many statistical instances recorded which is represented by the one to many relationship between Player Information and Player Stats. Player Stats stores information pertaining to the saves, goals scored, minutes played, and penalties of each player during each match for a specific team. Players can also have many Injury Reports which is represented by the one to many identifying relationship between Player Information and Injury Report. Injury report has information regarding the injury such as the reportID, type of injury that occurred, and estimated recovery timeline. 


Teams Have Matches stores information on the match date, venue and more. Teams Have Matches stores many player stats which is shown by the one to many identifying relationship between Player Stats and Teams Have Matches. 


Matches stores data on the match ID, match type and more. Matches is made up of many different individual matches which is represented by the one to many identifying relationship between Match and Teams Have Matches. 


Divisions store information on the division ID, the division name, the division age group, the division skill level and more. Divisions have many matches which is shown by the one to many non identifying relationship between Divisions and Match. Divisions are made up of many different teams which is represented by the one to many non identifying relationship between Divisions and Teams. 


The league entity stores data on the league ID, the league name, the league president, the date founded, and much more. A league is many up of many Divisions which is represented by the one to many non identifying relationship between League and Divisions. 


The Sponsor entity stores information including the sponsor ID, the sponsor name, and the phone number associated with the sponsor. A sponsor makes up a list of many different sponsors which is represented by the one to many identifying relationship between Sponsor and Teams Have Sponsors. The Teams Have Sponsors table is an associative entity created by the many to many relationship between Teams and Sponsors. The Teams Have Sponsors entity stores data such as the date of sponsorship and amount of sponsorship.


Coaching Staff stores data including the coach ID, the coach’s first and last name, the number of years they have coached, their date of birth, their date of birth, and much more. Coaching Staff at the football club report to Head Coaches which is shown by the one to many non identifying recursive relationship between Coaching Staff. Coaching Staff hold many training sessions which is represented by the one to many non identifying relationship between Coaching Staff and Training Sessions. 


Training Sessions store information on the session ID, the practice date, and more. Training Sessions can require many field reservations depending on the type of drills run which is represented by the one to many identifying relationship between Training Sessions and Field Reservation. Field reservations stores data including a composite primary key of fieldID and sessionID along with data such as reservation status and the date and time reserved.

![Data Model Soccer](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/ae4be42a-38b4-4ef0-93bf-a0ceacdf261a)

# Data Dictionary:
![Screenshot (359)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/2a997003-7f17-42ad-a221-847d4d22621d)

![Screenshot (344)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/c85f78dd-b9f2-4e1a-9ed2-ac2cd1fccf1f)

![Screenshot (345)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/18859b4b-bc07-40f5-99fe-d7ed531bd7c6)

![Screenshot (358)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/7e949830-5d27-4716-8fcb-c25b94c40a4d)

![Screenshot (347)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/2452956e-380b-49b7-ac6a-106c748c60a8)

![Screenshot (350)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/9737a48b-8324-475f-9d36-7c320292fd9e)

![Screenshot (360)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/94b8cab7-8aca-48c5-ad09-06da94edf618)

![Screenshot (352)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/bf288892-fc70-4dad-b2d6-f0443f869773)

![Screenshot (361)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/7296b756-46b3-4aca-8e4b-b7ea98dd6d1a)

![Screenshot (354)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/06f3e339-d845-42cc-81bf-ca9782c0d750)

![Screenshot (355)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/ae502dfa-04b4-411f-b251-0e6d8389eb5b)

![Screenshot (356)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/2aa916ab-b131-466b-9460-81f58c254cd4)

![Screenshot (362)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/2b124235-19d9-491b-8429-a672c7e3cd9d)

# Queries:
![Screenshot (341)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/0eff719d-fcd4-4d0b-a956-7a1007a9b55d)

1. Query 1 lists how the teams rank in terms of number of goals scored within their respective divisions and what percentage of the league total of goals scored each team accounts for.

![Screenshot (363)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/1b74b397-2567-44e3-8dc3-cb2563390bc1)

Query 1 allows the academy to see what teams score the most goals and their percentage share of total goals scored within the league. This information could be useful, as teams that score a higher percentage of goals in the league would be more likely to get moved to a higher skill division. Teams should be competitive in their division, but not overly competitive as this could result in a skill level imbalance.

2. Query 2 lists the players who are a captain for each team and the number of goals they have scored in their career at the academy. The results are ordered by the total number of goals they have scored descending.

![Screenshot (370)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/7b50f905-d188-4afe-8628-98b67c1ba0b6)

Query 2 shows the captains of each team and a ranking of captains by number of goals scored in their career at the Georgia United Soccer Academy. This information is useful in determining the most accomplished team captains for end of season awards and can help to determine future college soccer options.

3. Query 3 lists which coaches have canceled a practice and is ordered by the coach with the greatest number of cancellations descending.

![Screenshot (364)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/e10c96f4-768d-4879-b594-de553a96f7cd)

Query 3 allows the Georgia United Soccer Academy to see what coaches are canceling their field reservations and at what rate. This allows management to better manage field reservations, as coaches that tend to cancel their reservations most often get last pick after other coaches select their fields for practice.

4. Query 4 lists the total amount of how much sponsorship money each team has received. The results are ordered by the total amount of money received descending.

![Screenshot (365)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/92b0b4b2-25b5-4f0c-9d1f-5e79ba70be5e)

Query 4 shows the league how much money teams have received from their sponsors. This information can be used to spearhead fundraising and new sponsorship outreach efforts for teams with smaller cash inflows from sponsors. This can help teams keep down costs of travel and uniforms for its players.

5. Query 5 lists the first and last name of coaches that have coached more than 10 years who’s specialization is conditioning.

![Screenshot (366)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/fecb9fd1-1a92-442b-bb8b-65de058b446e)

Query 5 helps the Georgia United Soccer Academy identify conditioning coaches that may be up for promotion soon. The academy is always looking for Coaching Staff members that show loyalty and have coached for more than 10 years for promotions.

6. Query 6 lists the first and last names of players who are not on a team and the position they play.

![Screenshot (371)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/72026cc9-f0ad-4e47-91d4-432201fea1de)

Query 6 shows the soccer academy which players are available to join a team that are not already on one. This would allow coaches to search for players available to play certain positions where they may need another player and also lets the league know which children need to be placed with a team still. 

7. Query 7 lists the playerID, first name, last name, and number of penalties committed by players who have committed double the average penalties of an ordinary player in the league. The results are ordered by the number of penalties committed descending.

![Screenshot (367)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/aa9a7b0d-263d-413f-8b2a-c268734638f8)

Query 7 helps coaches and teams figure out which players are more likely to have penalties than others, which can be an important stat for teams to track about their own players, and their opponents. From a behavioral standpoint as this is a youth league, it is important to identify who is committing far more penalties than their peers in order to intervene while they are still developing. This data can be used by coaches to organize meetings with their players in order to correct this behavior.

8. Query 8 lists which players in the league have had a torn ACL before.

![Screenshot (372)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/5910dd88-05df-4740-850f-cc56ef215fdb)

Query 8 shows which players in the Football club have had an ACL injury before. This is important information for the club to keep track of a major injury like this that keeps players out for up to 9 months. If they have a lot of non contact injuries, they might want to consider moving from turf to grass or other preventative measures. In addition to this, the data will show which players are most prone to injury and coaches can take precautions to protect their players. 

9. Query 9 lists which coaches have more years of experience than the current head coach that they report to.

![Screenshot (368)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/f34c4735-3bb2-47a7-af68-4032021e5986)

Query 9 highlights potential organizational mismanagement within teams and shows the assistant coaches who have more experience than the current head coach they report to. If the season does not go well, this list would provide the basis for potential organizational restructuring and list the coaches who could become the new head coach on their current team.

10. Query 10 lists the number of goals scored by the winning team in each match classified as competitive and the results are ordered by matchID.

![Screenshot (369)](https://github.com/Rjk4133/MIST-Group4-Project-1/assets/148080194/ef222fb7-fb27-4b57-b77d-9d35007b4b5c)

Query 10 lists the total goals scored by a team that won or tied their match in matches that are classified as competitive. This is useful information as it provides a clear record of which team won each individual match in the matches that are competitive and can be used potentially as the basis of an exterior league standings table that assigns points based on wins and losses.

# Database Information:

Name of the database: ns_F2329704Group4

Additional Information: Each query listed above is marked in the database using stored procedures which can be called using the following format: "**CALL TP_QX()**" where X is equal to the query number.

# CHATGPT Logs:

https://chat.openai.com/share/1f833f36-10be-44eb-a8d2-274c12e57837













