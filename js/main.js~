


$(function(){ 
  
	// grid
	var $doc = $(document),
	    $body = $doc.find( 'body' ),
	    columns = 12,
	    rows, 
	    rowHeight = 12;

	//get screenwidth
	//get screenheight
	// devide sheight by height - insert that many rows
	

	
	// @grid
	// you need to check for changes and repeat
	var getScreenHeight = function(){ 
	    var screenHeight;
	    // get the height of the screen
	    return screenHeight = $(window).height();
	}

	// returns the needed rows for a flushed grid
	var getRowAmount = function( rowHeight, screenHeight ){ 
	    var rowAmount = screenHeight / rowHeight;
	    return rowAmount;
	}
		
	var makeGrid = function( columns,rows ){
	    var boxCount = 0;
	    
	    for( var int=0; int<rows; int++ ){ 
		for(var i=0; i<columns; i++){
		    $body.append( '<div class="box" data-box="'+ boxCount+'" data-box-status="empty"></div>');
		    boxCount ++;
		}//columns 
	    }//rows
	}
	

	//render
	$(window).on( 'load resize' , function(){ 
		// Test
		rows = Math.floor ( getRowAmount( rowHeight, getScreenHeight()) )
		makeGrid( columns, rows );

		
		// listen for box clicks
		$('[data-box]').on('click', function(){ 
			//
			var $this = $(this),
			    boxID = $this.attr( 'data-box' ),
			    boxStatus = $this.attr( 'data-box-status' );
			
			// make it a module
			if( boxStatus === 'empty' ){
			    
			    // make it a focused input
			    $this.append( '<input class="module" label="module name"/>' );
			    // get the input
			    $input = $this.find( 'input' ); 
			    // focus it
			    $input.focus();
			    // change status
			    $input.attr( 'data-box-status', 'edit' );
			    
			    // style it
			    $this.css({ 
				'background' : 'blue'
			    });
			    
			    //  YOU WHERE HERE

			    //listen for "enter"
			    $doc.keypress( function( event ) ){
				if( event.type === 13 ){ 
				    //convert
				}

			    }

			    //listen for outside click
			    
		    });
	    });
	
	

	// convert clicked boxes into inputs and save the outputs
	// all boxes under modules become features green
	// all boxes starting with if become yellow
	// all boxes ending with ! become actions
	// how do you nest? enter - you click out to leave the view
	// autofill covers module repetition
	    // box status possibilities
	    // view
	    // info
	    // conditional
	    // action
	    // module
	    // when active stauts === edit
    });
