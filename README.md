<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Leaderboard</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #121212;
            color: #ffffff;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        h1 {
            color: #ff9800;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
        }
        table {
            width: 100%;
            max-width: 800px;
            border-collapse: collapse;
            margin-top: 20px;
            background-color: rgba(40, 40, 40, 0.9);
            border-radius: 8px;
            overflow: hidden;
        }
        th, td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #333;
        }
        th {
            background-color: #ff9800;
            color: white;
        }
        tr:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }
        .rank {
            font-weight: bold;
        }
        .pagination {
            margin-top: 20px;
            text-align: center;
        }
        .pagination button {
            padding: 10px 15px;
            margin: 0 5px;
            background-color: #ff9800;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s, box-shadow 0.3s;
        }
        .pagination button:hover {
            background-color: #e68900;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }
        .pagination button:disabled {
            background-color: #ccc;
        }
    </style>
</head>
<body>

    <img src="https://files.oaiusercontent.com/file-8mH1pz1Yt4tHdXzXvnxvtM?se=2024-12-26T11%3A10%3A18Z&sp=r&sv=2024-08-04&sr=b&rscc=max-age%3D604800%2C%20immutable%2C%20private&rscd=attachment%3B%20filename%3D835095d0-873e-4f81-8bac-f6b83070cc1b.webp&sig=phOMJflAa1lIIYRTVeFwxhmEirJeo8Y2kvUeFp6EM5o%3D" style="width: 100%; max-width: 600px; display: block; margin: 0 auto;">
    <h1>Leaderboard</h1>


    <h1>Skill XP Rankings</h1>

    <div class="menu">
        <button onclick="showTable('melee')">Melee</button>
        <button onclick="showTable('magic')">Magic</button>
        <button onclick="showTable('mining')">Mining</button>
        <button onclick="showTable('smithing')">Smithing</button>
        <button onclick="showTable('woodcutting')">Woodcutting</button>
        <button onclick="showTable('crafting')">Crafting</button>
        <button onclick="showTable('fishing')">Fishing</button>
        <button onclick="showTable('cooking')">Cooking</button>
        <button onclick="showTable('spellbinding')">Spellbinding</button>
        <button onclick="showTable('totalxp')">Total XP</button>

</div>

    <!-- Skill Tables (existing definitions omitted for brevity) -->

  <!-- Total Xp Skill Table -->

<div id="totalXP" class="skill-table">
        <h2>Total Xp</h2>
        <table id="totalxpTable">
            <thead>
                <tr>
                    <th>Rank</th>
                    <th>Name</th>
                    <th>Level</th>
                    <th>XP</th>
                </tr>
            </thead>
            <tbody>
                <!-- Rows for Total Xp skill data -->
            </tbody>
        </table>
    </div>
  
<div id="melee" class="skill-table">
        <h2>Melee</h2>
        <table id="meleeTable">
            <thead>
                <tr>
                    <th>Rank</th>
                    <th>Name</th>
                    <th>Level</th>
                    <th>XP</th>
                </tr>
            </thead>
            <tbody>
     </table>
        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
    </div>           
<!-- Rows for Melee skill data -->
            </tbody>
        </table>
    </div>

  <!-- Magic Skill Table -->
<div id="magic" class="skill-table">
    <h2>Magic</h2>
    <table id="magicTable">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Level</th>
                <th>XP</th>
            </tr>
        </thead>
        <tbody>
    </table>
        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
    </div>       
 <!-- Rows for Magic skill data -->
        </tbody>
    </table>
</div>

<!-- Mining Skill Table -->
<div id="mining" class="skill-table">
    <h2>Mining</h2>
    <table id="miningTable">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Level</th>
                <th>XP</th>
            </tr>
        </thead>
        <tbody>
            <!-- Rows for Mining skill data -->
        </tbody>
   </table>

        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
</div>

<!-- Smithing Skill Table -->
<div id="smithing" class="skill-table">
    <h2>Smithing</h2>
    <table id="smithingTable">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Level</th>
                <th>XP</th>
            </tr>
        </thead>
        <tbody>
        </table>
        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
    </div>   
 <!-- Rows for Smithing skill data -->
        </tbody>
    </table>
</div>

<!-- Woodcutting Skill Table -->
<div id="woodcutting" class="skill-table">
    <h2>Woodcutting</h2>
    <table id="woodcuttingTable">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Level</th>
                <th>XP</th>
            </tr>
        </thead>
        <tbody>
    </table>
        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
    </div>        
<!-- Rows for Woodcutting skill data -->
        </tbody>
    </table>
</div>

<!-- Crafting Skill Table -->
<div id="crafting" class="skill-table">
    <h2>Crafting</h2>
    <table id="craftingTable">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Level</th>
                <th>XP</th>
            </tr>
        </thead>
        <tbody>
            </table>
        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
    </div>
<!-- Rows for Crafting skill data -->
        </tbody>
    </table>
</div>

<!-- Fishing Skill Table -->
<div id="fishing" class="skill-table">
    <h2>Fishing</h2>
    <table id="fishingTable">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Level</th>
                <th>XP</th>
            </tr>
        </thead>
        <tbody>
</table>
        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
    </div>
            <!-- Rows for Fishing skill data -->
        </tbody>
    </table>
</div>

<!-- Cooking Skill Table -->
<div id="cooking" class="skill-table">
    <h2>Cooking</h2>
    <table id="cookingTable">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Level</th>
                <th>XP</th>
            </tr>
        </thead>
        <tbody>
</table>
        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
    </div>
            <!-- Rows for Cooking skill data -->
        </tbody>
    </table>
</div>
<!-- SpellBinding Skill Table -->
<div id="spellbinding" class="skill-table">
    <h2>spellbinding</h2>
    <table id="spellbindingTable">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Level</th>
                <th>XP</th>
            </tr>
        </thead>
        <tbody>
</table>
        <div class="pagination">
            <button id="prevBtn" onclick="changePage(-1)">Previous</button>
            <button id="nextBtn" onclick="changePage(1)">Next</button>
        </div>
    </div>
            <!-- Rows for spellbinding skill data -->
        </tbody>
    </table>
</div>




   <script>
    // Existing players and skills
    const players = [
        {
            name: "FAME DDeY",
            skills: {
                melee: { level: 111, xp: 1302716115 },
                magic: { level: 114, xp: 1974716251 },
                mining: { level: 114, xp: 2202686040 },
                smithing: { level: 120, xp: 4536153492 },
                woodcutting: { level: 116, xp: 2777351696 },
                crafting: { level: 120, xp: 4536153492 },
                fishing: { level: 120, xp: 4536153492 },
                cooking: { level: 117, xp: 3275946599 },
                spellbinding: { level: 114, xp: 1974484997 },
                totalXP: { level: 1048, xp: 27116362174 }  // Added total XP
            }
        },
        {
            name: "FAME J1mms DiY",
            skills: {
                melee: { level: 94, xp: 123405994 },
                magic: { level: 99, xp: 260127468 },
                mining: { level: 107, xp: 749415878 },
                smithing: { level: 102, xp: 393651827 },
                woodcutting: { level: 120, xp: 4536153492 },
                crafting: { level: 120, xp: 4536153492 },
                fishing: { level: 114, xp: 2119987489 },
                cooking: { level: 106, xp: 673642799 },
                spellbinding: { level: 100, xp: 285758640 },
                totalXP: { level: 983, xp: 17612647141 } // Added total XP
            }
        },
        {
            name: "FAME N6N69",
            skills: {
                melee: { level: 110, xp: 1177905767 },
                magic: { level: 120, xp: 4536153492 },
                mining: { level: 119, xp: 4019428479 },
                smithing: { level: 110, xp: 1172775657 },
                woodcutting: { level: 120, xp: 4536153492 },
                crafting: { level: 100, xp: 291351206 },
                fishing: { level: 105, xp: 615947567 },
                cooking: { level: 90, xp: 73287938 },
                spellbinding: { level: 100, xp: 284208492 },
                totalXP: { level: 968, xp: 16517193290 } // Added total XP
            }
        },
        {
            name: "FAME Haise",
            skills: {
                melee: { level: 100, xp: 284866992 },
                magic: { level: 109, xp: 996931171 },
                mining: { level: 105, xp: 567131279 },
                smithing: { level: 105, xp: 567894582 },
                woodcutting: { level: 110, xp: 1140952035 },
                crafting: { level: 105, xp: 584730133 },
                fishing: { level: 105, xp: 597209716 },
                cooking: { level: 101, xp: 328750035 },
                spellbinding: { level: 100, xp: 284208492 },
                totalXP: { level: 942, xp: 5352674435 } // Added total XP
            }
        },
        {
            name: "FAME CriT",
            skills: {
                melee: { level: 85, xp: 36050941 },
                magic: { level: 96, xp: 173151190 },
                mining: { level: 120, xp: 4536153492 },
                smithing: { level: 110, xp: 1302146584 },
                woodcutting: { level: 120, xp: 4536153492 },
                crafting: { level: 102, xp: 424740924 },
                fishing: { level: 104, xp: 548360573 },
                cooking: { level: 100, xp: 321258800 },
                spellbinding: { level: 100, xp: 285758640 },
                totalXP: { level: 939, xp: 12163774636 } // Added total XP
            }
        },
        {
            name: "FAME OutLaww",
            skills: {
                melee: { level: 104, xp: 495343601 },
                magic: { level: 101, xp: 330763714 },
                mining: { level: 109, xp: 1004044693 },
                smithing: { level: 101, xp: 331561398 },
                woodcutting: { level: 100, xp: 285027413 },
                crafting: { level: 100, xp: 291402775 },
                fishing: { level: 110, xp: 1200714479 },
                cooking: { level: 110, xp: 1150125082 },
                spellbinding: { level: 100, xp: 290519396 },
                totalXP: { level: 937, xp: 5379502551 } // Added total XP
            }
        },
        {
            name: "FAME S E A L S",
            skills: {
                melee: { level: 116, xp: 2799070913 },
                magic: { level: 116, xp: 2776504342 },
                mining: { level: 105, xp: 577688499 },
                smithing: { level: 103, xp: 448414708 },
                woodcutting: { level: 105, xp: 596529584 },
                crafting: { level: 94, xp: 137025654 },
                fishing: { level: 100, xp: 289990624 },
                cooking: { level: 100, xp: 283660156 },
                spellbinding: { level: 92, xp: 96087683 },
                totalXP: { level: 933, xp: 8004972163 } // Added total XP
            }
        },
        // New Players
        {
            name: "FAME DigiPope",
            skills: {
                melee: { level: 104, xp: 531624935 },
                magic: { level: 107, xp: 764300120 },
                mining: { level: 100, xp: 283638705 },
                smithing: { level: 100, xp: 300907583 },
                woodcutting: { level: 100, xp: 293898446 },
                crafting: { level: 100, xp: 283549767 },
                fishing: { level: 107, xp: 820376596 },
                cooking: { level: 104, xp: 556354001 },
                spellbinding: { level: 100, xp: 283716938 },
                totalXP: { level: 924, xp: 4118367091 } // Added total XP
            }
        },
        {
            name: "FAME Cegii",
            skills: {
                melee: { level: 104, xp: 500790532 },
                magic: { level: 108, xp: 866521159 },
                mining: { level: 105, xp: 586187551 },
                smithing: { level: 101, xp: 325759865 },
                woodcutting: { level: 107, xp: 751286720 },
                crafting: { level: 95, xp: 152158811 },
                fishing: { level: 100, xp: 297120305 },
                cooking: { level: 99, xp: 277888939 },
                spellbinding: { level: 92, xp: 93598481 },
                totalXP: { level: 913, xp: 3851312363 } // Added total XP
            }
        },
        {
            name: "FAME FRATERNAL",
            skills: {
                melee: { level: 100, xp: 289457346 },
                magic: { level: 109, xp: 1027291537 },
                mining: { level: 100, xp: 291088648 },
                smithing: { level: 92, xp: 101649802 },
                woodcutting: { level: 120, xp: 4536153492 },
                crafting: { level: 95, xp: 156160841 },
                fishing: { level: 101, xp: 329240445 },
                cooking: { level: 95, xp: 142168559 },
                spellbinding: { level: 90, xp: 75400768 },
                totalXP: { level: 904, xp: 6948611438 } // Added total XP
            }
        },
        {
            name: "FAME Yaris",
            skills: {
                melee: { level: 112, xp: 1665668518 },
                magic: { level: 117, xp: 2992748233 },
                mining: { level: 104, xp: 493635288 },
                smithing: { level: 91, xp: 88675869 },
                woodcutting: { level: 101, xp: 359281221 },
                crafting: { level: 94, xp: 139457498 },
                fishing: { level: 101, xp: 332750605 },
                cooking: { level: 90, xp: 70996954 },
                spellbinding: { level: 90, xp: 74334818 },
                totalXP: { level: 902, xp: 6220401235 } // Added total XP
            }
        },
        {
            name: "FAME Sleepy",
            skills: {
                melee: { level: 83, xp: 28788236 },
                magic: { level: 105, xp: 638711128 },
                mining: { level: 101, xp: 344562799 },
                smithing: { level: 100, xp: 283702666 },
                woodcutting: { level: 104, xp: 498865838 },
                crafting: { level: 100, xp: 288247435 },
                fishing: { level: 104, xp: 523196348 },
                cooking: { level: 100, xp: 288836152 },
                spellbinding: { level: 100, xp: 300755346 },
                totalXP: { level: 899, xp: 3195665948 } // Added total XP
            }
        },
        {
            name: "FAME Crown",
            skills: {
                melee: { level: 97, xp: 187047360 },
                magic: { level: 104, xp: 527031317 },
                mining: { level: 100, xp: 322164907 },
                smithing: { level: 98, xp: 226077759 },
                woodcutting: { level: 111, xp: 1331787993 },
                crafting: { level: 93, xp: 108518670 },
                fishing: { level: 100, xp: 283513807 },
                cooking: { level: 100, xp: 283706312 },
                spellbinding: { level: 90, xp: 73174575 },
                totalXP: { level: 895, xp: 3343022700 } // Added total XP
            }
        },
        {
            name: "FAME Krueger",
            skills: {
                melee: { level: 101, xp: 358630327 },
                magic: { level: 104, xp: 549044722 },
                mining: { level: 100, xp: 283690164 },
                smithing: { level: 96, xp: 183904057 },
                woodcutting: { level: 97, xp: 201816497 },
                crafting: { level: 95, xp: 157580214 },
                fishing: { level: 101, xp: 362077750 },
                cooking: { level: 95, xp: 148071177 },
                spellbinding: { level: 100, xp: 283510651 },
                totalXP: { level: 891, xp: 2528325559 } // Added total XP
            }
        },
        {
            name: "FAME IssI",
            skills: {
                melee: { level: 101, xp: 325918949 },
                magic: { level: 112, xp: 1691464546 },
                mining: { level: 100, xp: 310683574 },
                smithing: { level: 95, xp: 147336408 },
                woodcutting: { level: 95, xp: 156345487 },
                crafting: { level: 91, xp: 92553397 },
                fishing: { level: 108, xp: 979566270 },
                cooking: { level: 93, xp: 115350695 },
                spellbinding: { level: 90, xp: 73316394 },
                totalXP: { level: 887, xp: 3892535720 } // Added total XP
            }
        },
        {
            name: "FAME Sparky",
            skills: {
                melee: { level: 98, xp: 214920118 },
                magic: { level: 106, xp: 656828486 },
                mining: { level: 93, xp: 116910657 },
                smithing: { level: 102, xp: 378049270 },
                woodcutting: { level: 107, xp: 774745750 },
                crafting: { level: 103, xp: 469888816 },
                fishing: { level: 95, xp: 144411756 },
                cooking: { level: 90, xp: 70890151 },
                spellbinding: { level: 90, xp: 76345573 },
                totalXP: { level: 886, xp: 2903052145 } // Added total XP
            }
        },
        {
            name: "FAME Gintoki",
            skills: {
                melee: { level: 104, xp: 509675859 },
                magic: { level: 104, xp: 516084538 },
                mining: { level: 104, xp: 552954427 },
                smithing: { level: 92, xp: 99266576 },
                woodcutting: { level: 112, xp: 1519514815 },
                crafting: { level: 100, xp: 286789450 },
                fishing: { level: 109, xp: 1072861543 },
                cooking: { level: 10, xp: 780 },
                spellbinding: { level: 90, xp: 73708180 },
                totalXP: { level: 827, xp: 4630856168 } // Added total XP
            }
        },
        {
            name: "FAME UttiiTghT",
            skills: {
                mining: { level: 101, xp: 343486115 },
                smithing: { level: 109, xp: 1021981043 },
                woodcutting: { level: 120, xp: 4536153492 },
                crafting: { level: 120, xp: 4536153492 },
                fishing: { level: 120, xp: 4536153492 },
                cooking: { level: 113, xp: 1724531035 },
                spellbinding: { level: 103, xp: 457440536 },
                totalXP: { level: 790, xp: 17155899249 } // Added total XP
            }
        },
        {
            name: "FAME Rushek",
            skills: {
                melee: { level: 93, xp: 107495558 },
                magic: { level: 103, xp: 445966480 },
                mining: { level: 80, xp: 18906731 },
                smithing: { level: 86, xp: 40750616 },
                woodcutting: { level: 96, xp: 180928313 },
                crafting: { level: 89, xp: 62678998 },
                fishing: { level: 74, xp: 8383850 },
                cooking: { level: 64, xp: 2185918 },
                spellbinding: { level: 91, xp: 88868828 },
                totalXP: { level: 780, xp: 971548965 } // Added total XP
            }
        },
        {
            name: "FAME NovsonGG",
            skills: {
                melee: { level: 84, xp: 33158826 },
                magic: { level: 109, xp: 1027775299 },
                mining: { level: 109, xp: 1040454771 },
                smithing: { level: 86, xp: 44414479 },
                woodcutting: { level: 91, xp: 85103156 },
                crafting: { level: 88, xp: 54975466 },
                fishing: { level: 90, xp: 73975113 },
                cooking: { level: 14, xp: 1740 },
                spellbinding: { level: 102, xp: 390549726 },
                totalXP: { level: 775, xp: 2756691536 } // Added total XP
            }
        },
        {
            name: "FAME malenia",
            skills: {
                magic: { level: 90, xp: 72121385 },
                mining: { level: 96, xp: 179681931 },
                smithing: { level: 94, xp: 135370210 },
                woodcutting: { level: 100, xp: 296597461 },
                crafting: { level: 94, xp: 126060236 },
                fishing: { level: 69, xp: 3922827 },
                cooking: { level: 66, xp: 2684821 },
                spellbinding: { level: 82, xp: 24012364 },
                totalXP: { level: 768, xp: 850597326 } // Added total XP
            }
        },
        {
            name: "FAME Overload",
            skills: {
                melee: { level: 100, xp: 312877390 },
                magic: { level: 94, xp: 132689711 },
                mining: { level: 66, xp: 2605531 },
                smithing: { level: 91, xp: 82855319 },
                woodcutting: { level: 65, xp: 2227189 },
                crafting: { level: 80, xp: 20042784 },
                fishing: { level: 68, xp: 3531334 },
                cooking: { level: 51, xp: 343408 },
                spellbinding: { level: 83, xp: 28846610 },
                totalXP: { level: 700, xp: 586019276 } // Added total XP
            }
        },
        {
            name: "FAME BUS",
            skills: {
                melee: { level: 103, xp: 441631690 },
                mining: { level: 104, xp: 559283275 },
                smithing: { level: 99, xp: 249249284 },
                woodcutting: { level: 97, xp: 193302973 },
                crafting: { level: 90, xp: 76711711 },
                fishing: { level: 63, xp: 1865315 },
                totalXP: { level: 621, xp: 1523462936 } // Added total XP
            }
        }
    ];

         const itemsPerPage = 5; // You can change this number to show more or fewer entries per page
        let currentPage = 1;
        let currentSkill = 'melee'; // Default skill table to display

        function showTable(skill) {
            // First, hide all skill tables
            const allTables = document.querySelectorAll('.skill-table');
            allTables.forEach(table => {
                table.style.display = 'none';
            });

            // Show the selected skill table
            const table = document.getElementById(skill);
            table.style.display = 'block';

            currentSkill = skill; // Update current skill
            currentPage = 1; // Reset to first page for new skill
            updateTable();
        }

        function updateTable() {
            const skillTable = document.getElementById(currentSkill).getElementsByTagName('tbody')[0];
            skillTable.innerHTML = ''; // Clear previous data

            // Sort players by the selected skill's XP
            const sortedPlayers = players.sort((a, b) => b.skills[currentSkill]?.xp - a.skills[currentSkill]?.xp);

            // Get the players to show on the current page
            const start = (currentPage - 1) * itemsPerPage;
            const end = start + itemsPerPage;
            const playersToShow = sortedPlayers.slice(start, end);

            // Populate the table with the players for the current page
            playersToShow.forEach((player, index) => {
                const row = skillTable.insertRow();
                row.insertCell(0).textContent = start + index + 1; // Rank
                row.insertCell(1).textContent = player.name; // Name
                row.insertCell(2).textContent = player.skills[currentSkill]?.level || 'N/A'; // Level
                row.insertCell(3).textContent = (player.skills[currentSkill]?.xp || 0).toLocaleString(); // XP
            });

            // Update pagination buttons visibility
            document.getElementById('prevBtn').disabled = currentPage === 1; // Disable prev button on first page
            document.getElementById('nextBtn').disabled = end >= sortedPlayers.length; // Disable next button if on last page
        }

        function changePage(direction) {
            currentPage += direction;
            updateTable();
        }

        // Show Melee table by default
        showTable('melee');
    </script>

</body>

</html>
