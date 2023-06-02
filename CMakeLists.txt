cmake_minimum_required(VERSION 3.1)

project(geos-inline-dev)

if(NOT EXISTS /usr/include/geos/geom.h)
  message(FATAL_ERROR "This package is only meant to supplement APT packages")
endif()

install(FILES
          CoordinateArraySequenceFactory.inl
          Coordinate.inl
          Envelope.inl
          GeometryCollection.inl
          GeometryFactory.inl
          LineSegment.inl
          MultiLineString.inl
          MultiPolygon.inl
          PrecisionModel.inl
          Quadrant.inl
        DESTINATION
          /usr/include/geos/geom/
)
