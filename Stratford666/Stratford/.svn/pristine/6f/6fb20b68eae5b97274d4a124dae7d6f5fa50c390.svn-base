	
	
/////////////////////////////////////////////////////	
/////////// Our code starts from  here :) ///////////
/////////////////////////////////////////////////////

var curTable = 1;
var selTable = 0;
var powerInfo = true;
var powerBoxDown = true;
var theTable = 1;


var powers= new Array("Tuesday July 8:", "Wednesday July 9:", "Thursday July 10:", "Friday July 11:", "Saturday July 12:", "Sunday July 13:");

var limboPowers = new Array("13 5 4ppp", "2poopo", "7tyyty", "4", "7", "3");		
var lustPowers = new Array("2", "3", "6", "4", "7", "7");
var gluttonyPowers = new Array("2", "7", "5", "7", "7", "4");
var greedPowers = new Array("4", "3", "6", "5", "2", "5");
var angerPowers = new Array("1", "6", "4", "4", "7", "3");
var heresyPowers = new Array("6", "6", "3", "5", "2", "6");
var violencePowers = new Array("7", "6", "2", "7", "1", "6");
var fraudPowers = new Array("6", "6", "3", "5", "2", "6");
var treacheryPowers = new Array("7", "6", "7", "7", "6", "7");



function showTable(selTable) 
{	
	// if the user selects the current art do nothing
	if (selTable == curTable)
	{
		//do nothing
		
	}
	else
	{	
			
		// else- hide the current table data
		$('#levelImage').animate(
		{
			marginLeft: -260
		}, 190, function(){swapTable(selTable);});
		
			
		// slide table data back in place
		$('#levelImage').animate(
		{
			marginLeft: 0,
			opacity: 1
		}, 250);
		
	
					
		// track/update curArt
		
	}
} //end showArt

function swapTable(selTable) // then - show the desired table (final table)
{	
	if (powerInfo == true)
	{
	 //don't fade info
	}
	else
	{
		$('#levelInfoDiv').fadeOut(90); // fade out
	}
	
	switch(selTable)
	{
		case 1: //Knockout Teams
		
		{	
			$('#circleTitle').html("Knockout Teams");
			$('#circleText').html(
			"<h3>Knockout Teams</h3>" +
			"An event in which a team (of four, five or six players, with four playing at a time) plays another team. The losers are eliminated or “knocked out” while the winners play other winners until only one winning team remains. The length of a KO match may vary from a single session to a full day (big events at the NABC tournaments) to a multi-day event (the Bermuda Bowl).");
			$('#levelImage').attr("src", "images/Alex.png");
			break;
		}
		
		case 2: // Brackedted Knockout Teams
		{
			$('#circleTitle').html("Bracketed Knockout Teams");
			$('#circleText').html(
			"<h3>Bracketed Knockout Teams</h3>" +
			"An event in which teams are divided into groups, usually of 8, 16 or 32 teams, based on their masterpoint holdings.The top group (Bracket I) and all other groups compete in a separate event with their own set of winners." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}
		
		case 3: //Compact Knockout Teams
		{
			$('#circleTitle').html("Compact Knockout Teams");
			$('#circleText').html(
			"<h3>Compact Knockout Teams</h3>" +
			"A shorter version of Bracketed KO teams. " );
			$('#levelImage').attr("src", "images/Helen.png");
			break;
		}
		
		case 4:  // Swiss Teams
		{
			$('#circleTitle').html("Swiss Teams");
			$('#circleText').html(
			"<h3>Swiss Teams</h3>" +
			"An event in which a team (of four, five or six players, with four playing at a time) plays other teams in seven-, eight- or nine-board matches.Team A sits North-South at Table 1 and East-West at Table 2 while Team B sits East-West at Table 1 and North-South at Table 2. The results are compared and scored by International Match Points (IMPs). Pairings for the first round are random. Pairings for succeeding rounds are determined by a team’s win-loss record or Victory Point total.  " );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}

		case 5: // International Match Points (IMPs) 
		{
			$('#circleTitle').html("International Match Points (IMPs)");
			$('#circleText').html(
			"<h3>Side Game Series</h3>" +

			"The most common method of scoring Swiss Team matches. Scoring example: if Team A scores plus 620 for bidding and making 4? on a particular deal and Team B scores only plus 170 (they didn’t bid the game), the difference is 450, which converts to 10 IMPs. The IMP chart is shown on the inside of your convention card.Point Difference	IMPs");
			$('#levelImage').attr("src", "images/Helen.png");
			break;
		}

		
		case 6: // Victory Points (VPs): 
		{
			$('#circleTitle').html("Victory Points (VPs)");
			$('#circleText').html(
			"<h3>Victory Points (VPs)</h3>" +

			"A method of scoring Swiss Team matches. After the scores are compared and converted to IMPs, the IMP total is converted to Victory Points. A team’s VP total may be used to determine its next opponents and its final standing." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}
		
		case 7: // Side Game Series
		{
			$('#circleTitle').html("Side Game Series");
			$('#circleText').html(
			"<h3>Side Game Series</h3>" +
			"A series of single-session pair games that pay red points. These series include at least three sessions and may have as many as six. You may play in as many sessions as you like, but only pairs who play in at least two sessions are eligible for overall gold points. Your best two sessions are used for determining overall winners." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}
		
		
		case 8: //Flighted Pairs:  
		{
			$('#circleTitle').html("Flighted Pairs");
			$('#circleText').html(
			"<h3>Flighted Pairs</h3>" +
			"When flighting is used, the field is divided by expertise or experience or both into several separate games. Flight A (“unlimited masterpoints”) will be open to all players while the remaining flights will be limited. Flight B might be 0-500 MPs or 0-1000 MPs while Flight C might be 0-300 or 0-500. Each flight is scored individually, and masterpoint awards are made for each flight. The masterpoint holdings of the players determine their flight. If one player is quite expert while his partner is new to the game, the pair must compete in Flight A. In flighted events, you may “play up” but not down. That means you may play in Flight A or Flight B even if your masterpoint holding qualifies you for Flight C. Conversely, you may not play in Flight B or Flight C if you are a Flight A player." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}
		
		case 9: // Stratified Pairs: 
		{
			$('#circleTitle').html("Stratified Pairs ");
			$('#circleText').html(
			"<h3>Stratified Pairs</h3>" +
			"A form of tournament pairs event in which entrants of different rank compete in different events, held simultaneously." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}

		case 10: // Matchpoints: 
		{
			$('#circleTitle').html("Matchpoints ");
			$('#circleText').html(
			"A form of tournament bridge scoring where a pair's score is compared against the score of the other pairs that sat in the same direction.  A pair wins one matchpoint for every pair it beats and a half for every pair it ties." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}

		case 11: // Pairs Event: 
		{
			$('#circleTitle').html("Pairs Event ");
			$('#circleText').html(
			"<h3>Pairs Events:</h3>" +
			"An event where pairs play against each other.  Usually, these events are scored in matchpoints." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}


		case 12: // Masterpoint: 
		{
			$('#circleTitle').html("Masterpoints ");
			$('#circleText').html(
			"<h3>Master Points</h3>" +
			"A rating system used by bridge organizations to categorize players based on skill and experience. Here is an explanation of <a href=\"http://www.acbl.org/masterpoints-results/masterpoint-awards-chart\" target=\"_blank\">ACBL Masterpoints</a>." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}

		case 13: // Teams: 
		{
			$('#circleTitle').html("Teams ");
			$('#circleText').html(
			"<h3>Teams</h3>" +
			"A form of scoring where two teams of 4, 5 or 6 players compare scores only against each other.  Team 1 will have a pair sitting North/South at table 1 and another pair sittng East/West at table 2.  Team 2 will have a piar sitting East/West at table 1 and a pair sitting North/South at table 2.  Both tables play all hands and compare scores after the play is over. The difference between the scores is cacluated and converted to International Match Points (IMPs)." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}

		case 14: // Directors: 
		{
			$('#circleTitle').html("Director ");
			$('#circleText').html(
			"<h3>Directors: </h3>" +
			"A director is an official at a tournament: sort of like a combination of a referee and a tournament organizer. When buying an entry, you will do so from a director or if there is some irregularity at the table during the play you would call for the director: (Director, Please!)" );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}
		case 15: // Kibitz: 
		{
			$('#circleTitle').html("Kibitz ");
			$('#circleText').html(
			"<h3>Kibitz</h3>" +
			"A spectator at a bridge table.  There are a number of famous stories about kibitzers at a bridge table, but it is generally accepted that they should be seen and not heard.  A Kibitzer should not affect the play of a hand in any way." );
			$('#levelImage').attr("src", "images/ChuckyY.png");
			break;
		}
		/*cases for the how to div*/
		case 16: // At a Tournament: 
		{
		
			$('#circleTitle').html("At a Tournament ");
			$('#circleText').html(
			"<h2>What to do at a Tournament </h2>" +
			"<p>When you arrive at a bridge tournament, you will find many people milling around and chatting at a hotel, conention center or some other social venue.  It all can be confusing if you don't know how it all comes together.</p>"+
			"<p>First, come early -- at least 15 minutes before game time.  If you are looking for a partner, come at least an hour before hand and go to the Partnership Desk.  The people at the Partnership Desk are there to help you find a partner of roughly the same skill level as you, so both of you can have an enjoyable session.  Don't worry about 'not being good enough' or that 'no one will want to play with you'.  Bridge is a social game and there are very many friendly people to help you enjoy your session.</p>"+
			"<p>At a tournament, you will find Directors, who are both the referees and run the session.  You can identify a director by the name badge or special shirt that he or she wears.  Directors have been trained in keeping and maintianing good relationships with player.  In many cases, the directors are very fine players in their own right.  Not only that, most diirectors are very interesting people with an interest in bridge -- just like you.  You will also see Caddies.  Generally caddies are teens and they are there to assist the directors.  They will pick up entry forms, deliver supplies to each table and, in a team event, transfer boards from one table to another.</p>"+
			"<p>When you have a partner, find the director's table where enties are being sold to the event you want to play.  This will be clearly marked, but if you are having trouble finding it, ask a director.  They are trained to help you through the process.  You will buy an entry, which looks like this:</p>"+
			
			"<br/><img src=\"/images/entry.png\" width=\"80%\"/><br/><br/>" +
			"<p>You and your partner fill out the personal information, including your ACBL number if you have one.  If you don't, don't worry about it.  Just make sure your name and city are clearly marked.  The entry will indicate which section you will be playing in -- usually a letter, like &quot;Section C&quot;; the table where you will start play and a direction: &quot;East/West&quot; or &quot;North/South&quot;.  You can identify your starting position as &quot;Table 5, North/South&quot; or &quot;Table 13, East/West&quot;.</p>"+
			"<p>As game time approaches, the directors will ask the players to go to their starting tables.  When everyone is seated, the directors will hand out the boards, containing the hands.  The cards will either be already shuffled and ready to play, or the hands will have to be sorted and set up (see shuffling cards).  Follow the directors' instructions.</p>"+ 
			"<p>When playing the hands, first remove the hand from the board, count the cards face down, so you can't see their values, to make sure you have 13, then look at and sort your hand.  Keep your hands seperate during the play and return your hand, again, face down to the correct slot in the board after the hand is over and record the score.</p>");
			//$('#levelImage').attr("src", "images/entry.png");
			break;

					
		}


		case 17: // Convention Cards 
		{
			$('#circleTitle').html("Convention Cards ");
			$('#circleText').html(
			"<h3>Convention Cards</h3>" +
			"<p>In the game of bridge, you are entitled to know what your opponents have agreed to about the meaning of certain bids and defensive plays.  In the same way, your opponents are allowed to know the agreements you have made with your partner.  Some partnerships may have a very simple set of agreements, where most bids are natural.  Some expert partnerships, especially those that have been playing together for years, might have a very complex set of agreements.  Each player at a tournament should have a completed convention card that summarizes a partnership’s agreements.  Each partner should have a card that is identical to his or her partner’s card.</p>"+ 
			"<p>This is a blank ACBL Convention Card.  You will find several stacks of these at the tournament.</p>"+
			"<br/><img src=\"/images/cc.png\" width=\"80%\"/><br/><br/>" +
			"<p>Your teacher will have been teaching you certain agreements about your bidding, perhaps the Stayman convention or that opening 1 Heart or 1 Spade shows at least five cards in that suit.  Your teacher can help you fill out your convention card for the tournament.</p>"+
			"<p>During the session, your opponent might ask to see your Convention Card – just as you can ask to see your opponent’s. If you need to ask for clarification, wait until it is your turn to bid or play and then ask the partner of the player who made the bid in question.</p>"+
			"<p></p>");
			//$('#levelImage').attr("src", "images/cc.png");
			break;
		}

		case 18: //Pairs Events: 
		{
			$('#circleTitle').html("Pairs Events ");
			$('#circleText').html(
			"<h3>Pairs Events</h3>" +
			 "<p>Two players compete as a partners throughout the event, whether it is one, two or more sessions.</p>" +
			 "<p>Computing your score is quite different from rubber bridge — it is based on matchpoints rather than on totals. You achieve a total score on each deal, but that score is then compared with all other scores achieved on that board.</p>" +
			 "<p>You earn one matchpoint for each score you surpass and half a matchpoint for each one you tie. In addition to overall awards, there are section awards for both North-South and East-West within a section.</p>" +
			 "<p>Generally you play two or three boards at a table—this is called a round—and then one pair (EW) moves to another table and plays other boards against other opponents.</p>" +
			 "<p>Scores for each hand, or board, are recorded and given to the director to tally the results of the entire game. Each pair has a number to identify them and this must also be entered on the scoresheet to show whose result it is.</p>" +
			 "<p>At the end of the whole session, each pair is awarded 1 matchpoint for each pair who scored worse than them on a board, and 1/2 matchpoint for each pair who scored equally.</p>" +
			 "<p>Then the total matchpoints scored by each pair over all the boards are calculated. This is generally converted to a percentage, for each pair, of the points they scored compared to the theoretical maximum.</p>"+
			 "<p>This gives a fair comparison between pairs who have played different numbers of boards.</p>" );
			break;
		}

		case 19: //Bidding Boxes: 
		{
			$('#circleTitle').html("Bidding Boxes");
			$('#circleText').html(
			"<h3>Bidding Boxes</h3>"+
			"<p>In an ACBL tournament, players bid by using bidding boxes.  These are the cards that hold the various call you can make during an auction: 1 Club up to 7 No Trump, Pass, Double (X) and Redouble (XX).  The reason we use them is to remove the inflection (and any added unauthorized information) that might be there in a spoken bid.</p>" +
			"<p>If you are passing, doubling or redoubling, place the card representing your call on the table in front of you.  If you are making a bid, out your thumb on the bidding card for the bid you want to make and take that card, plus all the cards underneath and put them in a neat pile on the table, with the card for your bid on top.  Your next call, choose the bidding card in the same way and place it overlapping the bids you have made before.  This means that the calls you have made in the auction remain exposed,</p>" +
			"<p>There are two special cards in the bidding box: the 'Stop' card and the 'Alert' card.  For the novice, the use of these cards will be limited.  If you need to understand their use, ask your teacher or a helpful director.</p>" +
			"<br/><img src=\"/images/bb-use.png\" width=\"80%\"/><br/><br/>");

			$('#levelImage').attr("src", "images/bb.png");

			break;
		}
		case 20: //The Director: 
		{
			$('#circleTitle').html("The Director ");
			$('#circleText').html(
			"<h3>The Director</h3>"+
			"<p>Some people see the director in the same way we view a policeman who is manning a speed trap – we would prefer to never see him. It is the director’s job to make sure no one is treated unfairly when a procedural error is committed.  It is better  to think of the director in the same way you would want your child to view a policeman – someone to go to for help.</p>"+ 
			"<p>Mistakes in play, what are called procedural errors, are not looked upon as opportunites to punish the offender. The rules of the game try to restore fairness instead of penalizing a player for breaking a rule.</p>"+
			"<p>When a procedural error occurs, such as bidding or leading out of turn, call the director immediately.  Most errors can be rectified, but inappropriate actions taken after a procedural error make it impossible to rectify the original error, often resulting in greater penalties than might have been assessed.</p>"+
			"<p>Here are the common errors and how to avoid them.</p>"+
			"<dl> "+
			"<dt>Incorrect number of cards:</dt>"+
			"<dd>Sometimes cards get mixed up when played at the previous table.    Try to keep the cards from each hand separate – you can be penalized after playing a hand if you cause a problem at the next table. <br/>To avoid causing a problem that cannot be corrected, count your cards face down (no peeking) before you look at them – if you hold fewer/more than 13 cards, call the director immediately.</dd>"+
            "<dt>Bidding out of Turn:</dt>"+
            "<dd>Before you take your cards out of the tray, be sure you know who is the dealer (and first bidder).  If you bid out of turn, your partner may be banned from bidding.  This might result in a poor score if you both have good hands.  Wait for your turn to bid.</dd>"+
            "<dt>Leading/playing out of turn:</dt>"+
            "<dd>If you lead or play out of turn, the opposition is often given some control of what cards you may play, and what suits you may lead.   Be sure to know who is declarer, and lead face down to start the play.  I always cite the contract and ask my partner if there are any questions before I lead.</dd>"+
            "<dt>Insufficient bid:</dt>"+
            "<dd>Sometimes a person will bid at an insufficient (too low) level e.g. 1NT - pass - 2H - 2D ??? The first solution to this error is NOT to make the bid sufficient. Call the director immediately.</dd>"+
            "<dt>Failure to Alert/Announce:</dt>"+
            "<dd>Some artificial bids must be announced (in blue on the convention card) such as transfers.  These conventions are announced by the bidder’s partner.   Other artificial bids must  be alerted (in red on the convention card) such as inverted minors.  Say “Alert” or use the Alert card, but do not explain the convention unless asked by an opponent.</dd>"+
			"</dl>" +
			"<p>Director Please: Duplicate bridge is a game with rules that ensure the game is fair for everyone.  You are not expected to memorize all the rules – you will learn them as you go. </p>");
			//$('#levelImage').attr("src", "images/cc.png");

			break;
		}
		
		case 21: //Table Etiquette 
		{
			$('#circleTitle').html("Table Etiquette ");
			$('#circleText').html(
			"<h3>Bridge Etiquette</h3>"+
			"<p>If there is a question about rules, politely call the director immediately. If you make an error and the director is called, don’t be intimidated.  A good director will politely present a ruling to make the situation fair to everyone in the  room.  If you are penalized, consider it a learning situation.  Smile and move on.</p>"+ 
			" <br/><ol>"+
			"<li>Although snapping the cards may sound musical to your ears, it can be very irritating to others. Quietly place your card on the table.</li>"+
			"<li>Take your hand off the card once you have played it. Holding it in your hand makes it hard for others at the table to see it.</li>"+
			"<li>Always lead before writing the contract down. This keeps other players from waiting. It also gives the declarer a few minutes to make his plan of play.</li>"+
			"<li>If you are making the opening lead:<ul>"+
			"<li>Lead face down and ask partner if there are any questions. This will keep you from leading out of turn.</li>"+
			"<li>Always lead before you write the contract down, the other three players needn’t wait.</li></ul></li>"+
			"<li>When you are declarer, avoid saying “play anything” from the dummy as this gives either 	opponent the opportunity to call the card from the dummy.</li>"+
			"<li>Wait until the end of the round to discuss hands. Even better, wait until the game is over. 	Voices carry. It is unfair to other players if you are overheard by the next table.</li>"+
			"<li>Wait until it is your turn to play a card. If partner is trying to decide which card to discard, a play out of turn by you might help with this decision.  Also, do not touch your cards until you are sure you know what card to play.</li>"+
			"<li>Once all cards in a trick are turned over, it is not permitted to ask to see that trick again.</li>"+
			"<li>Do not tell partner he has a trick turned the wrong way after you have played to the next trick. You may tell partner at the time of the mistake, however.</li>"+
			"<li>If a claim is made and you are not sure about it, call the director immediately.</li>"+
			"<li>A spectator, also known as a kibitzer must not display any reaction to the bidding or play. A spectator should be seated; it is annoying to have someone stand and look over your shoulder.</li>"+
			"<li>A player must use the red warning card of a skip (jump) bid always, or he must never 	use it. 	If a skip bid warning is made, the next player should pause about 10 seconds before 	making a bid. Even if the warning wasn’t given, the next bidder should wait 10 seconds 	(appear to be thinking about his next call). Perhaps it is easier, as a beginner, to never use the skip card.</li>"+
			"<li>Do not detach a card from your hand before it is your turn to play.  Don’t even reach for a 	card until it is your turn to play.  He same applies to bidding – know your bid before 	touching the bidding box.</li>"+
			"<li>Do not indicate approval or disapproval of a call or play.  However, you may compliment an 	opponent for good play or good bidding after a hand is played.</li></ol><br/>"+
			"<p>Following these simple do’s and don’ts increases the fun of the game for everyone involved and keeps the game running smoothly.</p><br/>");
			//$('#levelImage').attr("src", "images/cc.png");

			break;
		}

		case 22: // Zero Tolerance: 
		{
			
			$('#circleTitle').html("Zero Tolerance ");
			$('#circleText').html(
			"<h3>Zero Tolerance: </h3>"+
			" Traditionally, some bridge players in the past have had a reputation for poor behaviour at the table.  Back then, that kind of thing was accepted as part on the game.  These days, we are expected to treat our partners, teammates, opponents, directors, caddies and the hotel staff at the playing site with courtesy and respect."  +
			" Many actions by your opponents (and by your partner) can make you feel uncomfortable at the bridge table.  Unfortunately, a few “bad apples” have given a poor reputation to a great game.  When any behaviour by an opponent makes you feel uncomfortable, or nervous, or intimidated, you have some options:"  +
			"You can tell your opponents that their activity is detracting from your enjoyment of the game. If the activity persists or is repeated, call the director.  Never get in a discussion or argument with your opponents.  That would make you guilty of bad behaviour as well." +
			"If you are not comfortable talking to the opponents first, then call the director immediately."+  " Describe your problem to the director from your point of view: “the opponents comments to each other are making me nervous”, or “I feel intimidated by the opponent’s comments about my bidding”.  Do not say anything like “the opponents are arguing”, or “this player is criticizing my bidding."  +
			"Opponents are allowed to point out pleasantly that you are leading from the wrong hand, or that you have revoked, or that you bid out turn, or that it is not your lead, etc. " + 
			"Some people don’t like to call the director because they are not confident, or that they will create a bad relationship with the opponents.  If you feel that way, be prepared to tolerate the other team’s behaviour forever."  +
			"If your opponents regularly exhibit behaviour that bothers or offends you, the director may be happy to have a chance to deal with inappropriate behaviour that others tolerate."  +
			" If you perceive that a club does not enforce zero tolerance, then do not play at that club. If you do, prepare to be uncomfortable whenever you play there."  +
			"<h4>Here is a list of Do’s and Dont’s that will help you contribute to a good atmosphere. </h4>" +
			" <h1>Do's: </h1>                                          " +
			"<ul>" +
			"<li>Greet your opponents when they arrive at your table, or you arrive at theirs.</li>" +
			"               "+
			"<li>Save discussions of the hands for after the round is played (if there is time) or after the game.</li>" +
			"<li>Be mindful of the clock,  While it is important to think things out, the pace of play must be maintained.  If you get behind, you may have to skip a board.</li>"+  
			"<li>Congratulate opponents for a good play.  While it is OK to compliment partner for the same thing, make sure it is restrained, and does not appear to be gloating.</li>"+
			"<li> Do not leave trash at your table, both after the game and after a round.  Clean up ASAP.</li>" + 
			"<li>Thank your partner at the end of the round, no matter what the result.</li>" + 
			"<li>When you call the director, do so in a pleasant tone “Director, Please”.</li>"+
			"<li>If you eat or drink at the table (acceptable as long as it does not disrupt the bidding or play of the hand), be sure to keep the cards and the table clean.</li>" +
			"<li>Always have two identical convention cards available for the opponents to see.  They may reference your convention card at any point – you may only consult it between hands.</li>" +
			"<li>Be punctual – arrive early, get to your next table promptly after each round, chat after the round is completed (not before or during).</li>"+
			"<li>Be efficient – make your lead or place the dummy before you enter the contract on your score sheet.</li>"+
			"<li>Count your cards before you look at them.  If there are not 13 call the director.</li>" +
			"<li>Lead face down, and ask if there are any questions before you expose your card.  If it is your partner’s lead and you have no questions, say so  “No questions, partner”.</li>" +
			"<li>Keep your eyes on your own cards at your own table.</li>"+
			"<li>Play ethically at all times.  You will have more pride in your results.</li>" +
			"</ul><br/>"+
			"<h1> Don'ts:</h1>"+
			"<ul>"+
			"<li>Don’t gloat or celebrate when you get a high score on a hand.  This is poor sportsmanship.</li>" +
			"<li>Don’t wear perfume or after-shave – many people have allergies these days.</li>"+
			"<li>Don’t blame others if you have a problem or play slowly.  There is one exception – if the pair ahead of you are playing slowly, quietly bring it to the attention of the director, so you will not be blamed later. </li>"+
			"<li>Do not discuss the hands in a loud voice as this gives players at other tables an advantage.</li>"+
			"<li>Do not react to any problems at the table.  Making a face or shaking your head when partner makes an error is poor sportsmanship. Hide your frustration when things go wrong.</li>"+
			"</ul>");
            

			//$('#levelImage').attr("src", "images/cc.png");

			break;
		}

		case 23: //Kibitzers 
		{
			$('#circleTitle').html("Kibitzers ");
			$('#circleText').html(
			"<h3>Kibitzing</h3>" +
			"<p>Kibitzing is to watch another player play.  It has been a time honoured tradition to allow kibitzers at the bridge table.  Kibitzing a good player is an excellent way to learn more about the game.  There are a few rules and guidelines about being a good kibitzer.</p>" +
			"<p>Ask Permission to kibitz.  Most players are more than welcome to have a kibitzer, but there are a few who feel uncomfortable with one.  Asking is just good manners.  There are some people who feel uncomfortable with any kibitzer at the table and might ask you to leave, even it it is not him or her you are watching.  Any player can bar one kibitzer at the table without giving a reason, but after that, a kibitzer can be barred either for breaking a rule or if another player requests that a certain kibitzer be barred.  Generally, you want to keep good relations with all players at the table, so consider honouring a request even if a player is going beyond what is allowed.</p>" +
			"<p>Watch only one hand.  You are not allowed to look at another hand, even if you are sitting between two players.  If the player you are watching picks up a really bad hand, you are not allowed to look at the other hands, hoping to watch a player with a stronger hand.</p>" +
			"<p>No Talking. That includes to the players, or other kibitzers.  If you need to talk to someone, leave the table first.  Very rarely, a director might ask you about what happened at the table during some irregularity.  In this case, he or she will ask you about this away from the table, where the players cannot hear the conversation. </p>" +
			"<p>Save your questions for later. If you have any questions for the player about why he or she played a certain way, ask the player later.  Most experienced bridge players are more than happy to answer questions and give encouragement.  Contrary to the popular opinion, most great bridge players are approachable and welcome a thoughtful question or two from someone less experienced. </p>" +
			"<p>No Phones.  As a kibitzer, the same rules apply to you and your phone as it does to the players: the phone must be turned off and hidden from view.</p>" +
			"<p>No Reaction to the Play. You cannot react to a play in such a way that another player might read something into that play.  Making a face, sighing, shaking your head or any other indication is not permitted.  You are there to watch and not be watched. </p>" +
			"<p>Thank the Player. When you are finished kibitzing, it is good manners to thank the player for letting you watch.</p>"  );
			//$('#levelImage').attr("src", "images/cc.png");

			break;
		}
		case 24: //Bridge Mates 
		{
			$('#circleTitle').html("Bridge Mates ");
			$('#circleText').html(
			"<h2>BridgeMates</h2>" +
			"<p>Scoring at an ACBL Tournament is done using electronic terminals that wirelessly connect to a program on the Director’s computer.  These are usually referred to by their brand name: BridgeMates. </p>"+ 
			"<p>At the start of each session, all players at the table will be asked to enter their ACBL numbers (if they are members), but if they are not the directors will enter the names of the players into the scoring computer.</p>"+ 
			"<p>After each hand, the North Player at the table will enter the contract and the result, and the BridgeMate will be calculate the score.  North then asks either East or West to confirm the result and it is sent to the director’s computer.</p>"+ 
			"<p>Using BridgeMates might be a bit confusing at first, but once you are used to them, they are a much easier way of scoring than others – like pickup slips or travellers.  Teachers and directors will be available to help you get started, but you find them very easy to use and soon you will wonder why anyone would bother with other methods of reporting their scores.</p>"
			 );
			$('#levelImage').attr("src", "images/bridgemates.png");

			break;
		}
		case 25: //Shuffle 
		{
			$('#circleTitle').html("Shuffle ");
			$('#circleText').html(
			"<h3>Shuffling the Cards</h3>" +
			"<p>“Do we shuffle the cards?” is a common question of novices at a bridge tournament.  The answer is: it depends.  Some events will have the players shuffling the cards at various times and other events will have the players never shuffling.</p>" +
			"<p>If you are playing in a team event, ask the director if and when you need to shuffle the cards.  When you need to shuffle the cards, it is considered reasonable to riffle shuffle the cards </p>"+ 
			"<br/><br/>"+
			"<p>If you are playing in a pairs event, then the cards will have been ‘computer dealt’.  This means that the cards are more randomly shuffled (sometimes human shuffling is not as thorough as a computer) and that hand records, or printed sheets with the hands, are available after the session to review and discuss.</p>"+
			"<p>In most tournaments, a duplicating machine will be used and the boards will be ready for play.  The directors will distribute the boards, while announcing that the boards have been dealt and are ready for play.</p>"+
			"<p> If you need to ‘make’ the boards, the directors will hand out the boards, ask you to sort the cards into suits and then hand out slips of paper that have the hands to be played for the session.  Follow the directors’ instructions carefully if you have to do this.</p>");
			$('#levelImage').attr("src", "images/board.png");

			break;
		}
		
		case 26: //Teams 
		{
			$('#circleTitle').html("Teams Events ");
			$('#circleText').html(
			"<h2>Teams Events</h2>" +
			
			"<p>Teams of 4, 5 or 6 players play head to head against another team.</p>"+ 
			"<p>Suppose Team 1 is playing Team2.  At one table, a pair from Team 1 sits in the North/South positions and plays against a pair from Team 2, sitting East/West.  At another table, another pair from Team 2 sits North/South and plays against a pair from Team 1 sitting East/West. Both teams have four players sitting in the four directions.</p>"+
			"<p>Both tables play all the hands.  Usually a caddy is called when players need a board that will be at the other table.  A round may be as few as 6 boards (Swiss Teams) or up to 16 Boards or more (Knockouts). When the round is over, each team gathers to score the round.  For each hand, the points won at both tables are added.  The sum is converted to International Match Points (IMPs) according to this chart.  If the total is negative, you lose IMPs and if it is positive, you win IMPs. </p>"+
			"<p>When you total the IMPs won or lost for each hand, you have the result for that round.  In Swiss Teams, that IMP total is usually converted to Victory Points.  After the round, report the results to the director</p>"+
			"<table>"+
			"<tr><td><b>From:   </b></td><td><b>To:  </b></td><td><b>IMPs : </b> </td></tr><br/>" +
			""+
			"<tr><td>           0 -  </td>"+"<td>       10  </td>"+"<td>        0  </td></tr><br/>"+
			"<tr><td>          20 -  </td>"+"<td>       40  </td>"+"<td>        1  </td></tr><br/>"+
			"<tr><td>          50 -  </td>"+"<td>       80  </td>"+"<td>        2  </td></tr><br/>"+
			"<tr><td>          90 -  </td>"+"<td>      120  </td>"+"<td>        3  </td></tr><br/>"+
			"<tr><td>         130 -  </td>"+"<td>      160  </td>"+"<td>        4  </td></tr><br/>"+
			"<tr><td>         170 -  </td>"+"<td>      210  </td>"+"<td>        5  </td></tr><br/>"+
			"<tr><td>         220 -  </td>"+"<td>      260  </td>"+"<td>        6  </td></tr><br/>"+
			"<tr><td>         270 -  </td>"+"<td>      310  </td>"+"<td>        7  </td></tr><br/>"+
			"<tr><td>         320 -  </td>"+"<td>      360  </td>"+"<td>        8  </td></tr><br/>"+
			"<tr><td>         370 -  </td>"+"<td>      420  </td>"+"<td>        9  </td></tr><br/>"+
			"<tr><td>         430 -  </td>"+"<td>      490  </td>"+"<td>        10  </td></tr><br/>"+
			"<tr><td>         500 -  </td>"+"<td>      590  </td>"+"<td>        11  </td></tr><br/>"+
			"<tr><td>         600 -  </td>"+"<td>      740  </td>"+"<td>        12  </td></tr><br/>"+
			"<tr><td>         750 -  </td>"+"<td>      890  </td>"+"<td>        13  </td></tr><br/>"+
			"<tr><td>         900 -  </td>"+"<td>     1090  </td>"+"<td>        14  </td></tr><br/>"+
			"<tr><td>        1100 -  </td>"+"<td>     1290  </td>"+"<td>        15  </td></tr><br/>"+
			"<tr><td>        1300 -  </td>"+"<td>     1490  </td>"+"<td>        16  </td></tr><br/>"+
			"<tr><td>        1500 -  </td>"+"<td>     1740  </td>"+"<td>        17  </td></tr><br/>"+
			"<tr><td>        1750 -  </td>"+"<td>     1990  </td>"+"<td>        18  </td></tr><br/>"+
			"<tr><td>        2000 -  </td>"+"<td>     2240  </td>"+"<td>        19  </td></tr><br/>"+
			"<tr><td>        2250 -  </td>"+"<td>     2490  </td>"+"<td>        20  </td></tr><br/>"+
			"<tr><td>        2500 -  </td>"+"<td>     2990  </td>"+"<td>        21  </td></tr><br/>"+
			"<tr><td>        3000 -  </td>"+"<td>     3490  </td>"+"<td>        22  </td></tr><br/>"+
			"<tr><td>        3500 -  </td>"+"<td>     3990  </td>"+"<td>        23  </td></tr><br/>"+
			"<tr><td>        4000 -  </td>"+"<td>     UNLIMITED  </td>"+"<td>   24  </td></tr><br/>"+
			"</table>");
			//$('#levelImage').attr("src", "images/cc.png");

			break;
		}

		
		/*Handle any other subnav cases underneath*/		
		default:
		{
			// do nothing
			break;
		}
		
	}
	$('#levelInfoDiv').fadeIn(300); // fade out info div in
	curTable = selTable;	
} // end swapArt

function showPowers()
{
	powerInfo = true;
	showTable(curTable);
	
	$('#circleBox').animate(
	{
		height: 117,
	}, 180);
	
	powerBoxDown = true;
	setPowerHeaders();
	setPowerValues(curTable);
	
	
}
function hidePowers()
{	
	powerInfo = false;
	
	$('#circleBox').animate(
	{
		height: 1
	}, 180);
	
	powerBoxDown = false;
	setPowerHeaders();
	resetPowerValues();
	
}

function setPowerHeaders()
{
	if(powerBoxDown == true)
	{
		$('#powerHead1').html(powers[0]);
		$('#powerHead2').html(powers[1]);
		$('#powerHead3').html(powers[2]);
		$('#powerHead4').html(powers[3]);
		$('#powerHead5').html(powers[4]);
		$('#powerHead6').html(powers[5]);
	}
	else
	{
		$('#powerHead1').html("");
		$('#powerHead2').html("");
		$('#powerHead3').html("");
		$('#powerHead4').html("");
		$('#powerHead5').html("");
		$('#powerHead6').html("");
	}
}

//set Dante's circle or level stats and special features per level
function setPowerValues(theTable)
{
	switch(theTable)
	{
		case 1://Limbo
		{
			$('#powerValue1').html(limboPowers[0]);
			$('#powerValue2').html(limboPowers[1]);
			$('#powerValue3').html(limboPowers[2]);
			$('#powerValue4').html(limboPowers[3]);
			$('#powerValue5').html(limboPowers[4]);
			$('#powerValue6').html(limboPowers[5]);
			break;
		}
		
		case 2: //Lust
		{
			$('#powerValue1').html(lustPowers[0]);
			$('#powerValue2').html(lustPowers[1]);
			$('#powerValue3').html(lustPowers[2]);
			$('#powerValue4').html(lustPowers[3]);
			$('#powerValue5').html(lustPowers[4]);
			$('#powerValue6').html(lustPowers[5]);
			break;
		}
		case 3: //Gluttony
		{
			$('#powerValue1').html(gluttonyPowers[0]);
			$('#powerValue2').html(gluttonyPowers[1]);
			$('#powerValue3').html(gluttonyPowers[2]);
			$('#powerValue4').html(gluttonyPowers[3]);
			$('#powerValue5').html(gluttonyPowers[4]);
			$('#powerValue6').html(gluttonyPowers[5]);
			break;
		}
		
		case 4: //Greed
		{
			$('#powerValue1').html(greedPowers[0]);
			$('#powerValue2').html(greedPowers[1]);
			$('#powerValue3').html(greedPowers[2]);
			$('#powerValue4').html(greedPowers[3]);
			$('#powerValue5').html(greedPowers[4]);
			$('#powerValue6').html(greedPowers[5]);
			break;
		}
		
		case 5: //Anger
		{
			$('#powerValue1').html(angerPowers[0]);
			$('#powerValue2').html(angerPowers[1]);
			$('#powerValue3').html(angerPowers[2]);
			$('#powerValue4').html(angerPowers[3]);
			$('#powerValue5').html(angerPowers[4]);
			$('#powerValue6').html(angerPowers[5]);
			break;
		}
		
		case 6: //Heresy
		{
			$('#powerValue1').html(heresyPowers[0]);
			$('#powerValue2').html(heresyPowers[1]);
			$('#powerValue3').html(heresyPowers[2]);
			$('#powerValue4').html(heresyPowers[3]);
			$('#powerValue5').html(heresyPowers[4]);
			$('#powerValue6').html(heresyPowers[5]);
			break;
		}
		
		case 7: //Violence
		{
			$('#powerValue1').html(violencePowers[0]);
			$('#powerValue2').html(violencePowers[1]);
			$('#powerValue3').html(violencePowers[2]);
			$('#powerValue4').html(violencePowers[3]);
			$('#powerValue5').html(violencePowers[4]);
			$('#powerValue6').html(violencePowers[5]);
			break;
		}
		case 8: //Fraud
		{	
			$('#powerValue1').html(fraudPowers[0]);
			$('#powerValue2').html(fraudPowers[1]);
			$('#powerValue3').html(fraudPowers[2]);
			$('#powerValue4').html(fraudPowers[3]);
			$('#powerValue5').html(fraudPowers[4]);
			$('#powerValue6').html(fraudPowers[5]);
			break;
		}		
		
		case 9: //Treachery
		{
			$('#powerValue1').html(treacheryPowers[0]);
			$('#powerValue2').html(treacheryPowers[1]);
			$('#powerValue3').html(treacheryPowers[2]);
			$('#powerValue4').html(treacheryPowers[3]);
			$('#powerValue5').html(treacheryPowers[4]);
			$('#powerValue6').html(treacheryPowers[5]);
			break;
		}


		default: //nothing
		{
				//no broke
				break;
		}
	}		
}
function resetPowerValues()
{
	$('#powerValue1').html("");
	$('#powerValue2').html("");
	$('#powerValue3').html("");
	$('#powerValue4').html("");
	$('#powerValue5').html("");
	$('#powerValue6').html("");
}
