# calculator
Sourece Code
using System;

namespace Taxiapp
{
  public class Taxi
  {
    public string DriverName {get; set;}
    public bool OnDuty;
    public int NumPassenger {get; set;}

    public void TaxiInfo()
    {
      Console.WriteLine("Driver Name : {0}", DriverName);
      if (OnDuty == true)
      {
        Console.WriteLine("On Duty : Yes ");
      }
      else
      {
        Console.WriteLine("On Duty : No ");
      }

      Console.WriteLine("Number of Passenger : {0}", NumPassenger);
      Console.WriteLine();
    }

    public void PickUpPassenger()
    {
      Console.WriteLine("{0} sedang menjemput penumpang", DriverName);
    }

    public void DropOffPassenger()
    {
      Console.WriteLine("{0} selesai mengantar penumpang", DriverName);
    }
  }

  class PROGRAM
  {
    static void Main(string[] args)
    {
      Console.WriteLine();
      Taxi taxi = new Taxi();

      taxi.DriverName = "Jono";
      taxi.OnDuty = true;
      taxi.NumPassenger = 10;

      taxi.TaxiInfo();
      taxi.PickUpPassenger();
      taxi.DropOffPassenger();

      Console.ReadKey();
    }
  }
}
