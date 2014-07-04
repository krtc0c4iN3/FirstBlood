//Init background var
var backGroundY = 0;
var backGroundShift = 0.005;

//Character Var
var charX = 0.5, charY = 0.8;
var charW = 0.16, charH = 0.115;

function OnStart()
{

 app.SetOrientation( "Portrait" );
 app.PreventScreenLock( true );
 
 //Main Layout
 lay = app.CreateLayout( "linear", "FillXY" );
 
 
 //This space reserved for blank canvas
 canvas = app.CreateImage( null, 1.0, 1.0, "fix", 480, 800 );
 canvas.SetAutoUpdate( false );
 canvas.SetTextSize( 12 );
 canvas.SetPaintColor("#ffff0000");
 canvas.SetOnTouchMove( canvas_OnTouchMove );
 lay.AddChild( canvas );
 
 //Background Image
 imgBackground = app.CreateImage("insertfilehere.jpg")
 
 //Character Image
 imgChar = app.CreateImage("insertcharacterimghere.jpg.");
 
 //App_layout
 app.AddLayout( lay );
 
 app.SetDebugEnabled( false );
 
 //Game Frame
 timer = setInterval( DrawFrame, 1000/30 );
 }
 
 //Game graphics update
 function DrawFrame()
 {
   canvas.Clear();
   canvas.DrawImage( imgBackground, 0, -1.0 + backGroundY, 1.0, 1.0 );
   canvas.DrawImage( imgBackground, 0, backGroundY, 1.0, 1.0 );
   
 //Shifting the background images downwards
 backGroundY += backGroundShift;
 if( backGroundY >= 1.0 ) backGroundY -= 1.0;
 
 //Draw Character
 canvas.DrawImage( imgChar, charX, charY, charW, charH );
 
 canvas.Update()
 }
 
 function canvas_OnTouchMove( ev )
 {
   if( ev.Y > 0.8 )
      charX = ev.X - charW/2;
 }
 
 
 

