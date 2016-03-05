# live_basketball_analysis
In-Game Analysis Using StatBroadcast

*************************************************************************************
README FOR LIVE BASKETBALL ANALYTICS SCRIPTS
ANDRES GRANADA – ANDRESG1869@GMAIL.COM
ERIC DUPRE – EDUPRE7@LSU.EDU
*************************************************************************************
THESE R PROGRAMS WERE DEVELOPED AS THE BASIS FOR AN ANALYTICS PROJECT WITH A COLLEGIATE MEN’S BASKETBALL TEAM. WE PROCESS DATA FROM THE PLAY BY PLAY PROVIDER, STATBROADCAST FOR THE PURPOSES OF IN-GAME ANALYSIS AND SUPPLEMENTING OUR SEASON-LONG DATABASE. WE AIM TO HAVE THIS PROGRAM GENERAL ENOUGH THAT OTHER BASKETBALL PROGRAMS OR SPORTS ANALYTICS ORGANIZATIONS CAN USE IT BY SIMPLY UPDATING ONE’S WORKING DIRECTORY, STATBROADCAST URL FOR THE CURRENT GAME, WHETHER THE GAME IS HOME/AWAY, AND ONE’S “STAR PLAYER”. WITH THESE INPUTS SPECIFIED, THE PROGRAMS WILL PROCESS LIVE GAME DATA, PROVIDING BASIC AND ADVANCED STATS AT THE INDIVIDUAL, LINEUP, AND TEAM LEVEL FOR BOTH TEAMS. ALL RELEVANT DATA ARE OUTPUT IN .CSV FORMAT SO THAT THEY CAN BE EASILY INCORPORATED INTO YOUR SEASON-LONG STATISTICS DATABASE. ADDITIONALLY, ONE TEXT FILE, “PRINT” IS OUTPUT, PROVIDING A SUMMARY OF THE DATA ANALYZED. “PRINT” CONTAINED ALL OF THE RELEVANT DATA WE WERE INTERESTED IN LIVE, BUT THIS CAN BE UPDATED TO SUIT YOUR NEEDS.

IN THE REST OF THIS DOCUMENT, WE GIVE AN OVERVIEW OF OUR GOALS AND AN OUTLINE OF THE TWO SCRIPTS WE’VE CREATED. PLEASE FEEL FREE TO CONTACT EDUPRE7@LSU.EDU OR ANDRESG1869@GMAIL.COM WITH ANY QUESTIONS OR CONCERNS.

IN THIS PROGRAM, WE HAVE TWO GOALS:
1.       PROVIDE REAL TIME ANALYSIS OF BOX SCORE AND PLAY BY PLAY DATA

2.       SAVE DATA AND ANALYSIS FOR FURTHER ANALYSIS THROUGHOUT THE SEASON

3.    OUR TEAM WAS INTERESTED IN ANALYZING SITUATIONS WHEN CERTAIN PLAYERS WERE IN/OUT OF THE GAME, SO WE ADDED THE “STAR PLAYER” FUNCTIONALITY. ESSENTIALLY, THIS FEATURE ADDS VARIABLES CALLED “GAME SEGMENT” AND “HALF SEGMENT” TO THE LINEUP BOX SCORE, CHANGING EVERY TIME THIS “STAR PLAYER’ COMES IN OR LEAVES THE GAME. YOU CAN READ MORE ABOUT THIS FEATURE IN THE PROGRAMS THEMSELVES.

IN ORDER TO ACHIEVE THESE OBJECTIVES, WE HAVE SPLIT OUR PROJECT INTO TWO SCRIPTS:
1.       FUNTIONS (PART ONE)- DEFINES AND SAVES FUNCTIONS WE’VE DEVELOPED TO REDUCE CLUTTER IN THE PROCESSING SCRIPT AND ALLOW OUR ANALYSES TO BE RUN MORE EFFICIENTLY FOR BOTH HOME AND AWAY TEAMS. WE’VE DEVELOPED FUNCTIONS TO AGGREGATE BASIC TEAM STATS (POINTS, REBOUNDS, ASSISTS, ETC.), ADVANCED STATS (POINTS IN THE PAINT, 2ND CHANCE POINTS, ETC), AND CALCULATED STATS (GAME SCORE, OFFENSIVE EFFICIENCY RATING, ETC). IN ADDITION, WE HAVE A FUNCTION THAT PROCESSES PLAY BY PLAY DATA SUCH THAT WE CAN CREATE A BOX SCORE FOR LINEUPS FOR BOTH TEAMS THAT INCLUDES BASIC STATS (MINUTES PLAYED, POINTS, ASSISTS, ETC) AND ADVANCED STATS (PLUS MINUS, GAME SCORE, ETC). IN THIS SCRIPT, THERE IS AN OBJECT DEFINED AS “USER CONTROL”, WHICH ALLOWS THE USER TO SPECIFY WHICH SEGMENT OF THE GAME TO PROCESS (HALF 1/ HALF 2) MANUALLY, IGNORING THE CURRENT STATUS OF THE GAME. WE INCLUDED THIS FEATURE SO THAT USERS CAN RUN THESE ANALYSES ON PAST GAMES, ANALYZE OTHER GAMES OF INTEREST, OR RE-DO THE ANALYSIS ON THE CURRENT GAME, SHOULD AN ERROR ARISE. 

2.       PROCESSING (PART TWO)- THIS IS THE MAIN SCRIPT THAT SCRAPES THE WEB FOR THE DATA WE NEED AND PROCESSES THEM TO CALCULATE ADVANCED STATS. SPECIFICALLY, WE ARE INTERESTED IN THE HOME AND AWAY TEAM BOX SCORES, PLAY BY PLAY, AND THE ADVANCED TEAM STATS THAT STATBROADCAST PROVIDES. ONCE THE DATA ARE LOADED INTO R, THE FUNCTIONS FROM THE FIRST SCRIPT ARE CALLED TO ASSIST IN PROCESSING/ ANALYSIS. FINALLY, THIS SCRIPT OUTPUTS DATA THAT CAN BE USED FOR OUT OF GAME PROCESSING OR IN-GAME SHARING.
YOU CAN FIND SPECIFIC COMMENTS IN THE PROGRAMS THEMSELVES.
 

