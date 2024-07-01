speed detector code
function speeddetect() {
    let speed = prompt("Please enter the car's speed (in km/h):");
  
    
    speed = Number(speed);
  
    
    if (isNaN(speed) || speed < 0) {
      console.log("Invalid input. Please enter a valid number.");
      alert("Invalid input. Please enter a valid number.");
      return;
    }
  
    
    const speedLimit = 70;
    const kmPerDemeritPoint = 5;
    const maxDemeritPoints = 12;
  
    
    if (speed < speedLimit) {
      console.log("Ok");
      alert("Ok");
    } else {
      
      const demeritPoints = Math.floor((speed - speedLimit) / kmPerDemeritPoint);
  
      if (demeritPoints > maxDemeritPoints) {
        console.log("License suspended");
        alert("License suspended");
      } else {
        console.log(`Points: ${demeritPoints}`);
        alert(`Points: ${demeritPoints}`);
      }
    }
  }
  
  // Call the function to prompt the user and check the speed
  speeddetect()  
