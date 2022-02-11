DayZ Deer Isle PC "Flight System Heliz" Mod by RedFalcon PC Install Instructions & Terms Of Use

Many thanks to RedFalcon for creating this amazing mod. Please visit his Discord, https://discord.io/redfalconmodz
and sub to his YouTube: https://www.youtube.com/channel/UCznA3EuyfHuISNjqtNOs0jg

THIS IS AN EARLY SET OF FILES SO SERVER OWNERS CAN EASILY SPAWN IN FULLY WORKING HELICOPTERS WITHOUT USING ADMIN TOOLS OR TRADER.
THESE FILES WILL PROBABLY BE SUPERCEDED AS RED FALCON CREATES HIS OWN XMLS.

Spawn fully working(you just need to add fuel, which is included in cargo) Helo's at various points on Deer Isle. (See photos in Github)

THIS IS NOT RedFalcon's OFFICIAL INSTALL INSTRUCTIONS AND IS NOT AFFILIATED WITH RED FALCON.

Limited Testing on PC Deer Isle Local Server DAYZ Version 1.15 Feb 2022.

XML snippets Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

PLEASE SEE THE README INSIDE THE Flight System Heliz MOD FOR RedFalcon's TERMS OF USE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Ensure you have an up-to-date version on Deer Isle, and it's Mission Files, working on your Community or Local Server.

Subscribe to Flight System Heliz on Steam:

https://steamcommunity.com/sharedfiles/filedetails/?id=2692979668

Start your DayZ Launcher to download the mod files. Using your FTP programme, copy the @RedFalcon Flight System Heliz folder from your DayZ !workshop folder
to the root directory of your server. Copy the key from the mods key folder to your servers key folder. Edit your start batch file,
so that your server will load @RedFalcon Flight System Heliz mod on startup. (On Nitrado and some other DayZ Server Providers you don't have access to the batch file,
instead you will find an "Additional mods" setting in the settings section of your servers web interface, add @RedFalcon Flight System Heliz there.)

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Stop your server using it's web control panel.

Using FTP or your Servers file browser, make the following additions to your XMLS:

Open your events.xml file (its in the db folder on your server) and add the following XML snippet at the top, below the <events> tag:

<!-- red falcons helis events addtitions-->


 <event name="VehicleRFFSHeli_Bo105m">
        <nominal>3</nominal>
        <min>3</min>
        <max>3</max>
        <lifetime>300</lifetime>
        <restock>0</restock>
        <saferadius>500</saferadius>
        <distanceradius>2</distanceradius>
        <cleanupradius>200</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>fixed</position>
        <limit>mixed</limit>
        <active>1</active>
        <children>
            <child lootmax="0" lootmin="0" max="3" min="3" type="RFFSHeli_Bo105m"/>
        </children>
    </event>

 <event name="VehicleRFFSHeli_LittleBird">
        <nominal>3</nominal>
        <min>3</min>
        <max>3</max>
        <lifetime>300</lifetime>
        <restock>0</restock>
        <saferadius>500</saferadius>
        <distanceradius>2</distanceradius>
        <cleanupradius>200</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>fixed</position>
        <limit>mixed</limit>
        <active>1</active>
        <children>
            <child lootmax="0" lootmin="0" max="3" min="3" type="RFFSHeli_LittleBird"/>
        </children>
    </event>
	
	 <event name="VehicleRFFSHeli_Bell429">
        <nominal>2</nominal> 
        <min>2</min>
        <max>2</max>
        <lifetime>300</lifetime>
        <restock>0</restock>
        <saferadius>500</saferadius>
        <distanceradius>2</distanceradius>
        <cleanupradius>200</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>child</position>
        <limit>mixed</limit>
        <active>1</active>
        <children>
            <child lootmax="0" lootmin="0" max="2" min="2" type="RFFSHeli_Bell429"/>
        </children>
    </event>
	
	 <event name="VehicleRFFSHeli_Ka26">
        <nominal>5</nominal> 
        <min>5</min>
        <max>5</max>
        <lifetime>300</lifetime>
        <restock>0</restock>
        <saferadius>500</saferadius>
        <distanceradius>2</distanceradius>
        <cleanupradius>200</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>fixed</position>
        <limit>mixed</limit>
        <active>1</active>
        <children>
            <child lootmax="0" lootmin="0" max="5" min="5" type="RFFSHeli_Ka26"/>
        </children>
    </event>
	

<!-- end of red falcons helis event additions -->


Open your types.xml file (its in the db folder on your server) and add the following XML snippet at the top, below the <types> tag:

<!--red falcons heli types additions-->
  <type name="RFFSHeli_Bo105m">
        <nominal>0</nominal>
        <lifetime>1296000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_Bo105m_wreck">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_LittleBird">
        <nominal>0</nominal>
        <lifetime>1296000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_LittleBird_Camo">
        <nominal>0</nominal>
        <lifetime>1296000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_LittleBird_Desert">
        <nominal>0</nominal>
        <lifetime>1296000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_LittleBird_wreck">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_Ka26">
        <nominal>0</nominal>
        <lifetime>1296000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_Ka26_wreck">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_Bell429">
        <nominal>0</nominal>
        <lifetime>1296000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_Bell429_wreck">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_Katran_wreck">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_Osprey_static">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_flight_case">
       <nominal>20</nominal>
        <lifetime>28800</lifetime>
        <restock>1800</restock>
        <min>10</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFFSHeli_hydraulic_hoses">
       <nominal>20</nominal>
        <lifetime>28800</lifetime>
        <restock>1800</restock>
        <min>10</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
        <category name="tools" />
        <usage name="Industrial" />
        <tag name="floor" />
    </type>
    <type name="RFFSHeli_wiring_harness">
       <nominal>20</nominal>
        <lifetime>28800</lifetime>
        <restock>1800</restock>
        <min>10</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
        <category name="tools" />
        <usage name="Industrial" />
        <tag name="floor" />
    </type>
    <type name="RFFSHeli_igniter_plug">
        <nominal>20</nominal>
        <lifetime>28800</lifetime>
        <restock>1800</restock>
        <min>10</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
        <category name="tools" />
        <usage name="Industrial" />
        <tag name="floor" />
    </type>
    <type name="RFFSHeli_aviation_battery">
       <nominal>20</nominal>
        <lifetime>28800</lifetime>
        <restock>1800</restock>
        <min>10</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
        <category name="tools" />
        <usage name="Industrial" />
        <tag name="floor" />
    </type>
    <type name="RFFSHeli_aviation_toolbox">
       <nominal>20</nominal>
        <lifetime>28800</lifetime>
        <restock>1800</restock>
        <min>10</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
        <category name="tools" />
        <usage name="Industrial" />
        <tag name="floor" />
    </type>
    <type name="RFFSHeli_hydraulic_fluid">
        <nominal>20</nominal>
        <lifetime>28800</lifetime>
        <restock>1800</restock>
        <min>10</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
        <category name="tools" />
        <usage name="Industrial" />
        <tag name="floor" />
    </type>
	
	<!-- end of red flacons helis types additions-->
	
Save the file and re-upload if necessary.

Open your cfgspawnabletypes.xml file (its in the root folder of the mission folder on your server) and add the following XML snippet,
just below <damage min="0.3" max="0.7" /> which is near the top of the file:

		<!-- start of red falcons heli spawnabletypes -->
	
	<type name="RFFSHeli_Bo105m">
		<attachments chance="1.00">
			<item name="RFFSHeli_hydraulic_hoses" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_wiring_harness" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_igniter_plug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_battery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_toolbox" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_hydraulic_fluid" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_flight_case" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_battery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="ZSh3PilotHelmet" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Deagle" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Mag_Deagle_9rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Mag_Deagle_9rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="AmmoBox_357_20Rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="PistolSuppressor" chance="1.00" />
		</attachments>
	</type>
	
	<type name="RFFSHeli_LittleBird">
		<attachments chance="1.00">
			<item name="RFFSHeli_hydraulic_hoses" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_wiring_harness" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_igniter_plug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_battery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_toolbox" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_hydraulic_fluid" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_battery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_flight_case" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="ZSh3PilotHelmet" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Deagle" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Mag_Deagle_9rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Mag_Deagle_9rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="AmmoBox_357_20Rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="PistolSuppressor" chance="1.00" />
		</attachments>
	</type>
	
	<type name="RFFSHeli_Bell429">
		<attachments chance="1.00">
			<item name="RFFSHeli_hydraulic_hoses" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_wiring_harness" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_igniter_plug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_battery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_toolbox" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_battery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_hydraulic_fluid" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_flight_case" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="ZSh3PilotHelmet" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Deagle" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Mag_Deagle_9rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Mag_Deagle_9rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="AmmoBox_357_20Rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="PistolSuppressor" chance="1.00" />
		</attachments>
	</type>
	
	<type name="RFFSHeli_Ka26">
		<attachments chance="1.00">
			<item name="RFFSHeli_hydraulic_hoses" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_wiring_harness" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_igniter_plug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_battery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_battery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_aviation_toolbox" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_hydraulic_fluid" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="RFFSHeli_flight_case" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="ZSh3PilotHelmet" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Deagle" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Mag_Deagle_9rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Mag_Deagle_9rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="AmmoBox_357_20Rnd" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="PistolSuppressor" chance="1.00" />
		</attachments>
	</type>
	
	
	
	<!--end of red falcons spawnabletypes additions-->
	
	
	Open your cfgeventspawns.xml file (its in the root folder of the mission folder on your server) and add the following XML snippet,
just below <eventposdef> which is near the top of the file:
	
	<!-- red falcons heli spawns event spawns additions-->

<event name="VehicleRFFSHeli_Bo105m"> 
		<pos x="5522.93" z="3606.96" a="-57.1379"/><!-- Main Airfield -->
		<pos x="5491.72" z="3631.28" a="0"/><!-- Main Airfield -->
		<pos x="1679.00" z="15700.33" a="6.53697"/><!-- Swans Island Airfield-->
    </event>

<event name="VehicleRFFSHeli_LittleBird"> 
		<pos x="5724.27" z="3707.8" a="175.638"/><!-- Main Airfield -->
		<pos x="5706.5"  z="3695.55" a="173.472"/><!-- Main Airfield -->
		<pos x="13441.9"  z="9626.55" a="-19.5479"/><!-- Area 42 Airfield-->
	</event>
	
	<event name="VehicleRFFSHeli_Bell429"> 
		<pos x="5432.35" z="3744.52" a="171.761"/><!-- Main Airfield -->
		<pos x="5455.73" z="3728.03" a="-171.514"/><!-- Main Airfield -->
	</event>
	
	<event name="VehicleRFFSHeli_Ka26"> 
		<pos x="5780.09" z="3602.05" a="-10.4198"/><!-- Main Airfield -->
		<pos x="5811.72" z="3599.71" a="-11.9189"/><!-- Main Airfield -->
		<pos x="1654.00" z="15645.28" a="-3.80821"/><!-- Swans Island Airfield --> 
		<pos x="13489.5" z="9684.62" a="-179.595"/><!-- Area 42 Airfield-->
		<pos x="8888.43" z="5976.93" a="34.0505"/><!-- Camp Bear -->
	</event>

<!-- end of red falcons heli event spawns additions -->

Save your changes & upload if you need to.

Restart your server and the Helos will be spawning in for the enjoyment of your players!!!!!

Thanks again to RED FALCON

Please join his Discord: https://discord.io/redfalconmodz
and sub to his YouTube: https://www.youtube.com/channel/UCznA3EuyfHuISNjqtNOs0jg 

Thanks, Rob.