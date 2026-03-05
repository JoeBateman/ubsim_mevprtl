art_make_library( LIBRARY_NAME sbncode_EventGenerator_MeVPrtl_Constants
          SOURCE Constants.cpp
          LIBRARIES
                            ROOT::Core
                            ROOT::Eve
                            ROOT::X3d
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
        )

cet_make_library(
  LIBRARY_NAME ubsim_Common_EventGen_MeVPrtl
  SOURCE
    MeVPrtlTruth.cxx
    MesonParent.cxx
  LIBRARIES
    cetlib_except::cetlib_except
    nusimdata::SimulationBase
    dk2nu::Tree
  )

art_dictionary(DICTIONARY_LIBRARIES ubsim_Common_EventGen_MeVPrtl nusimdata::SimulationBase)

add_library(ubsim::ubsim_Common_EventGen_MeVPrtl ALIAS ubsim_Common_EventGen_MeVPrtl)


cet_build_plugin( MeVPrtlGen art::module
          LIBRARIES
              art::Framework_Core
              art::Framework_Services_Registry
              art_root_io::TFileService_service
              art_root_io::TFileService_service
              art_root_io::tfile_support
              art::Framework_Principal
              art::Persistency_Common
              art::Utilities canvas::canvas
              cetlib::cetlib cetlib_except::cetlib_except
              CLHEP::CLHEP
              nugen::EventGeneratorBase_GENIE
              nusimdata::SimulationBase
              larcorealg::Geometry
              lardata::Utilities
              nurandom::RandomUtils_NuRandomService_service
              larcoreobj::SummaryData
              ubsim_Common_EventGen_MeVPrtl
              sbncode_EventGenerator_MeVPrtl_Constants
)

cet_build_plugin( MeVPrtlTestRayTrace art::module
                    LIBRARIES
                        art::Framework_Core
                        art::Framework_Services_Registry
                        art_root_io::TFileService_service
                        art_root_io::TFileService_service
                        art_root_io::tfile_support
                        art::Framework_Principal
                        art::Persistency_Common
                        art::Utilities canvas::canvas
                        cetlib::cetlib cetlib_except::cetlib_except
                        CLHEP::CLHEP
                        nugen::EventGeneratorBase_GENIE
                        nurandom::RandomUtils_NuRandomService_service
                        nusimdata::SimulationBase
                        larcoreobj::SummaryData
                        ubsim_Common_EventGen_MeVPrtl
                        sbncode_EventGenerator_MeVPrtl_Constants
                        lardata::Utilities
)


cet_build_plugin( EmptyKaonGen art::tool
                       LIBRARIES
                            art::Framework_Core
                            art::Framework_Services_Registry
                            art_root_io::TFileService_service
                            art::Framework_Principal
                            art::Persistency_Common
                            art::Utilities canvas::canvas
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
                            ROOT::Eve
                            ROOT::X3d
                            ROOT::Core
                            dk2nu::Tree
                            CLHEP::CLHEP
                            nugen::EventGeneratorBase_GENIE
                            nurandom::RandomUtils_NuRandomService_service
                            nusimdata::SimulationBase
                            sbncode_EventGenerator_MeVPrtl_Constants
                           ubsim_Common_EventGen_MeVPrtl
)


cet_build_plugin( NuMiKaonGen art::tool
                       LIBRARIES
                            ifdh_art::IFDH_service
                            art::Framework_Core
                            art::Framework_Services_Registry
                            art_root_io::TFileService_service
                            art::Framework_Principal
                            art::Persistency_Common
                            art::Utilities canvas::canvas
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
                            ROOT::Eve
                            ROOT::X3d
                            ROOT::Core
                            CLHEP::CLHEP
                            ifdh::ifdh
                            dk2nu::Tree
                            nurandom::RandomUtils_NuRandomService_service
                            nusimdata::SimulationBase
                            sbncode_EventGenerator_MeVPrtl_Constants
                           ubsim_Common_EventGen_MeVPrtl
)

cet_build_plugin( TxtFileGen art::tool
                      LIBRARIES
                            ifdh_art::IFDH_service
                            art::Framework_Core
                            art::Framework_Services_Registry
                            art_root_io::TFileService_service
                            art::Framework_Principal
                            art::Persistency_Common
                            art::Utilities canvas::canvas
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
                            ROOT::Eve
                            ROOT::X3d
                            ROOT::Core
                            CLHEP::CLHEP
                            ifdh::ifdh
                            dk2nu::Tree
                            nurandom::RandomUtils_NuRandomService_service
                            nusimdata::SimulationBase
                            sbncode_EventGenerator_MeVPrtl_Constants
                           ubsim_Common_EventGen_MeVPrtl
)
                            
cet_build_plugin( BNBKaonGen art::tool

                       LIBRARIES
                            ifdh_art::IFDH_service
                            art::Framework_Core
                            art::Framework_Services_Registry
                            art_root_io::TFileService_service 
                            art::Framework_Principal
                            art::Persistency_Common
                            art::Utilities canvas::canvas
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
                            ROOT::Eve
                            ROOT::X3d
                            ROOT::Core
                            CLHEP::CLHEP
                            ifdh::ifdh
                            dk2nu::Tree
                            nurandom::RandomUtils_NuRandomService_service
                            nusimdata::SimulationBase
                            sbncode_EventGenerator_MeVPrtl_Constants
                           ubsim_Common_EventGen_MeVPrtl
)

cet_build_plugin( WeightedRayTraceBox art::tool
                       LIBRARIES
                            art::Framework_Core
                            art::Framework_Services_Registry
                            art_root_io::TFileService_service
                            art::Framework_Principal
                            art::Persistency_Common
                            art::Utilities canvas::canvas
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
                            ROOT::Eve
                            ROOT::X3d
                            ROOT::Core
                            CLHEP::CLHEP
                            larcorealg::Geometry
                            larcore::Geometry_Geometry_service
                            nurandom::RandomUtils_NuRandomService_service
                            nusimdata::SimulationBase
                            dk2nu::Tree
                            sbncode_EventGenerator_MeVPrtl_Constants
                           ubsim_Common_EventGen_MeVPrtl
)

cet_build_plugin( MixedWeightRayTraceBox art::tool
                       LIBRARIES
                            art::Framework_Core
                            art::Framework_Services_Registry
                            art_root_io::TFileService_service
                            art::Framework_Principal
                            art::Persistency_Common
                            art::Utilities canvas::canvas
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
                            ROOT::Eve
                            ROOT::X3d
                            ROOT::Core
                            dk2nu::Tree
                            CLHEP::CLHEP
                            larcorealg::Geometry
                            larcore::Geometry_Geometry_service
                            nurandom::RandomUtils_NuRandomService_service
                            nusimdata::SimulationBase
                            sbncode_EventGenerator_MeVPrtl_Constants
                           ubsim_Common_EventGen_MeVPrtl
)




cet_build_plugin( ReThrowRayTraceBox art::tool
                       LIBRARIES
                            art::Framework_Core
                            art::Framework_Services_Registry
                            art_root_io::TFileService_service
                            art::Framework_Principal
                            art::Persistency_Common
                            art::Utilities canvas::canvas
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
                            ROOT::Eve
                            ROOT::X3d
                            ROOT::Core
                            CLHEP::CLHEP
                            larcorealg::Geometry
                            larcore::Geometry_Geometry_service
                            nurandom::RandomUtils_NuRandomService_service
                            nusimdata::SimulationBase
                            sbncode_EventGenerator_MeVPrtl_Constants
                           ubsim_Common_EventGen_MeVPrtl
)

cet_build_plugin( RayTraceBox art::tool
                       LIBRARIES
                            art::Framework_Core
                            art::Framework_Services_Registry
                            art_root_io::TFileService_service
                            art::Framework_Principal
                            art::Persistency_Common
                            art::Utilities canvas::canvas
                            fhiclcpp::fhiclcpp
                            cetlib::cetlib cetlib_except::cetlib_except
                            ROOT::Eve
                            ROOT::X3d
                            ROOT::Core
                            CLHEP::CLHEP
                            larcorealg::Geometry
                            larcore::Geometry_Geometry_service
                            nurandom::RandomUtils_NuRandomService_service
                            nusimdata::SimulationBase
                            sbncode_EventGenerator_MeVPrtl_Constants
                           ubsim_Common_EventGen_MeVPrtl
)

add_subdirectory(Higgs)
add_subdirectory(HNL)
add_subdirectory(ALP)

install_headers()
install_fhicl()
install_source()
