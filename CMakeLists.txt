cmake_minimum_required(VERSION 3.20)

project(lexilla
        VERSION 5.1.5
        DESCRIPTION "A library of language lexers for use with Scintilla "
        LANGUAGES CXX
        )

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


add_library(${PROJECT_NAME}
        src/Lexilla.cxx
        access/LexillaAccess.cxx
        access/LexillaAccess.h
        lexlib/Accessor.cxx
        lexlib/Accessor.h
        lexlib/CatalogueModules.h
        lexlib/CharacterCategory.cxx
        lexlib/CharacterCategory.h
        lexlib/CharacterSet.cxx
        lexlib/CharacterSet.h
        lexlib/DefaultLexer.cxx
        lexlib/DefaultLexer.h
        lexlib/LexAccessor.cxx
        lexlib/LexAccessor.h
        lexlib/LexerBase.cxx
        lexlib/LexerBase.h
        lexlib/LexerModule.cxx
        lexlib/LexerModule.h
        lexlib/LexerNoExceptions.cxx
        lexlib/LexerNoExceptions.h
        lexlib/LexerSimple.cxx
        lexlib/LexerSimple.h
        lexlib/OptionSet.h
        lexlib/PropSetSimple.cxx
        lexlib/PropSetSimple.h
        lexlib/SparseState.h
        lexlib/StringCopy.h
        lexlib/StyleContext.cxx
        lexlib/StyleContext.h
        lexlib/SubStyles.h
        lexlib/WordList.cxx
        lexlib/WordList.h
        lexers/LexA68k.cxx
        lexers/LexAbaqus.cxx
        lexers/LexAda.cxx
        lexers/LexAPDL.cxx
        lexers/LexAsciidoc.cxx
        lexers/LexAsm.cxx
        lexers/LexAsn1.cxx
        lexers/LexASY.cxx
        lexers/LexAU3.cxx
        lexers/LexAVE.cxx
        lexers/LexAVS.cxx
        lexers/LexBaan.cxx
        lexers/LexBash.cxx
        lexers/LexBasic.cxx
        lexers/LexBatch.cxx
        lexers/LexBibTeX.cxx
        lexers/LexBullant.cxx
        lexers/LexCaml.cxx
        lexers/LexCIL.cxx
        lexers/LexCLW.cxx
        lexers/LexCmake.cxx
        lexers/LexCOBOL.cxx
        lexers/LexCoffeeScript.cxx
        lexers/LexConf.cxx
        lexers/LexCPP.cxx
        lexers/LexCrontab.cxx
        lexers/LexCsound.cxx
        lexers/LexCSS.cxx
        lexers/LexDataflex.cxx
        lexers/LexD.cxx
        lexers/LexDiff.cxx
        lexers/LexDMAP.cxx
        lexers/LexDMIS.cxx
        lexers/LexECL.cxx
        lexers/LexEDIFACT.cxx
        lexers/LexEiffel.cxx
        lexers/LexErlang.cxx
        lexers/LexErrorList.cxx
        lexers/LexEScript.cxx
        lexers/LexFlagship.cxx
        lexers/LexForth.cxx
        lexers/LexFortran.cxx
        lexers/LexFSharp.cxx
        lexers/LexGAP.cxx
        lexers/LexGDScript.cxx
        lexers/LexGui4Cli.cxx
        lexers/LexHaskell.cxx
        lexers/LexHex.cxx
        lexers/LexHollywood.cxx
        lexers/LexHTML.cxx
        lexers/LexIndent.cxx
        lexers/LexInno.cxx
        lexers/LexJSON.cxx
        lexers/LexJulia.cxx
        lexers/LexKix.cxx
        lexers/LexKVIrc.cxx
        lexers/LexLaTeX.cxx
        lexers/LexLisp.cxx
        lexers/LexLout.cxx
        lexers/LexLua.cxx
        lexers/LexMagik.cxx
        lexers/LexMake.cxx
        lexers/LexMarkdown.cxx
        lexers/LexMatlab.cxx
        lexers/LexMaxima.cxx
        lexers/LexMetapost.cxx
        lexers/LexMMIXAL.cxx
        lexers/LexModula.cxx
        lexers/LexMPT.cxx
        lexers/LexMSSQL.cxx
        lexers/LexMySQL.cxx
        lexers/LexNim.cxx
        lexers/LexNimrod.cxx
        lexers/LexNsis.cxx
        lexers/LexNull.cxx
        lexers/LexOpal.cxx
        lexers/LexOScript.cxx
        lexers/LexPascal.cxx
        lexers/LexPB.cxx
        lexers/LexPerl.cxx
        lexers/LexPLM.cxx
        lexers/LexPO.cxx
        lexers/LexPOV.cxx
        lexers/LexPowerPro.cxx
        lexers/LexPowerShell.cxx
        lexers/LexProgress.cxx
        lexers/LexProps.cxx
        lexers/LexPS.cxx
        lexers/LexPython.cxx
        lexers/LexRaku.cxx
        lexers/LexR.cxx
        lexers/LexRebol.cxx
        lexers/LexRegistry.cxx
        lexers/LexRuby.cxx
        lexers/LexRust.cxx
        lexers/LexSAS.cxx
        lexers/LexScriptol.cxx
        lexers/LexSmalltalk.cxx
        lexers/LexSML.cxx
        lexers/LexSorcus.cxx
        lexers/LexSpecman.cxx
        lexers/LexSpice.cxx
        lexers/LexSQL.cxx
        lexers/LexStata.cxx
        lexers/LexSTTXT.cxx
        lexers/LexTACL.cxx
        lexers/LexTADS3.cxx
        lexers/LexTAL.cxx
        lexers/LexTCL.cxx
        lexers/LexTCMD.cxx
        lexers/LexTeX.cxx
        lexers/LexTxt2tags.cxx
        lexers/LexVB.cxx
        lexers/LexVerilog.cxx
        lexers/LexVHDL.cxx
        lexers/LexVisualProlog.cxx
        lexers/LexX12.cxx
        lexers/LexYAML.cxx
        )

target_link_libraries(${PROJECT_NAME} scintilla-qt-edit)
target_include_directories(${PROJECT_NAME} PUBLIC
        include/
        )
target_include_directories(${PROJECT_NAME} PRIVATE
        access/
        lexlib/
        include/
        scintilla/include
        )
set_property(TARGET ${PROJECT_NAME} PROPERTY VERSION "${CMAKE_PROJECT_VERSION}")
set_property(TARGET ${PROJECT_NAME} PROPERTY SOVERSION 5 )

# TODO - this part is too ugly, and should not be here
if ("${CMAKE_CXX_COMPILER_ID}" MATCHES "Clang")
    target_compile_options(${PROJECT_NAME} PRIVATE -Wall -Wextra -pedantic --warn-no-unused-variable -Wformat -Wformat-security)
elseif ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "GNU")
    target_compile_options(${PROJECT_NAME} PRIVATE -Wall -Wextra -pedantic --warn-no-unused-variable -Wformat -Wformat-security)
elseif ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "Intel")
    MESSAGE("TODO: Intel compiler uses generic builds - add better compile flags")
elseif ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "MSVC")
    target_compile_options(${PROJECT_NAME} PRIVATE /utf-8 /guard:cf)
    target_link_options(${PROJECT_NAME} PRIVATE /guard:cf)
endif()
